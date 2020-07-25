---
layout: post
title: What We Talk About When We Talk About Zeitgeist
date: '2016-06-05 19:10:00'
---

There is a tangible confusion around as to what Zeitgeist is and what it isn’t; what it can do and what it can’t do. This is partly our own fault because we could have communicated this whole thing better, for instance we have some very outdated wiki pages lying around that you should probably stay away from until we updated them. In this post I aim to give a semi technical run down of the core Zeitgeist functionality and how we expose it for you to work with. This should hopefully clear out some confusion.

### Events
The Zeitgeist daemon (also known as the engine) is a process that exposes an event logging framework as a DBus API. The structure of these events is that they have a block of metadata that describe the event itself (this is known simply as the event metadata) and another block of metadata that describes the subject, or subjects, that this event happened to (this part is known as the subject metadata). The metadata for the event looks like:

* **Timestamp** – When did this happen. Milliseconds since the Unix Epoch. Note that we see events as single points in time, meaning that events don’t have a duration
* **Interpretation** – Abstract interpretation of this event; what happened. Fx. “opened”, “saved”, “closed”, “send”, etc.
* **Manifestation** – How the event happened. Fx. “user activity”, “notification”, or “scheduled activity”.
* **Actor** – Who triggered it. This will typically point to the .desktop file of the acting application. It will most likely be an application, but it is not required to be so.
* **Payload** – A free-form binary blob that you may attach to the event. This is specifically application specific and mainly intended to be a “back door” for people to do all sorts of funky hacks.

Each event has one or more subjects associated. For each subject we store:

* **URI** – You guessed it! The URI of the subject
* **Interpretation** – Abstract interpretation of the subject. This could be “Document”, “Image”, “Video”, “Email”, “Instant message”, “Contact”, anything.
* **Manifestation** – How the subject is stored. This could be something like “File”, “Mailbox”, “Web page”.
* **Origin** – A URI pointing to the origin or “patron” of the subject. For files this would be the parent folder. For YouTube videos it would be http://youtube.com
* **Mimetype** – The format of the datastream representing the subject. Fx. text/plain, application/xml.
* **Text** – Textual information added to the subject. This is not applicable for for types of subjects.
* **Storage** – Identifier for the storage medium this subject resides on. We use this to make it possible for queries that return only events for subjects that are “available now”. Fx. some clients don’t want to show events for files that are stored on you USB pen drive when it is not connected.


### Ontology – Or Data Description
In reality the metadata fields we store don’t contain simple strings like “Document” for the subject interpretation. It’s a bit more complex than that – sorry! We store a URI pointing to a formal definition of something categorized as a Document. This formal categorization is called an ontology if you want a word to confuse your friends with. We are fortunate enough that someone already wrote such a spec, namely the Nepomuk Ontology. So instead of just “Document” we store the string ”http://www.semanticdesktop.org/ontologies/2007/03/22/nfo/#Document“.

Since Tracker also uses the Nepomuk ontologies you may take these formal classification strings and plug them directly into Tracker to find everything that Tracker considers a document.

We will also have an ontology for the event metadata as this is not covered by Nepomuk. We are actively working on this.

### Getting Data Out – Querying the Event Log
We employ a template based query API for searching our log data. You send us a list of event templates you want to look for and how you want it sorted and we give you the results. So if you want to find all “open” events on subjects of type “Document” simply create an Event object, set the interpretaion to “open”-event and add a subject to the event template with the interpretation set to “document”. All other fields should be left blank. Send this template to us and we will give you the matches.

The list of event templates is collected into a big OR-query to imbue the consumers with more power.

### Getting Data Into Zeitgeist
There are really no limits to what kind of events we could store. If you have a spare mobile with a in-built accelerometer and glue it to your front door then you could send an event over bluetooth to your desktop each time your front door opens. Probably there are better use cases?

The point is that the usefulness of Zeitgeist stands and falls with the events that you push into us. We can store anything that you can model using the structures I outlined above. I am pretty certain that people will not agree on the kinds of data they want logged, but we are ready for anything :-)

Normal users would of course not need to think about getting their data into Zeitgeist. What developers need to know is that we have a simple DBus API to insert events (surprisingly called InsertEvents). It is called InsertEvents and not AppendEvents or something like that for a reason. Namely that you are allowed to insert events that are in the past. This is useful if you want to import your Firefox history or what ever. If you try to log an event twice the engine will throw an error at you, so no need to worry about dupes.

Ok. I think that about wraps up what I intended to say for now. Hope it’s useful to at least one person out there! :-)
