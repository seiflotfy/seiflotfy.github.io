---
layout: post
title: Understanding the Event Centric Experience
date: '2009-06-29 00:58:32'
---

Application Centric Experience (ACE), e.g: Every Application knows the documents it touched.
Document Centric Experience (DCE), e.g: Every Document knows the applications that touched it.

Event Centric Experience(ECE): ACE U DCE

The only constant variable on your computer are events. If no events are happening then computer can not be running.
An event consists of minimum 5 variables:

1) Timestamp: time of the event
2) Subject: The application
3) Object: The target (Document)
4) Type: Activity (the user does something thus triggers an Event) or Notification(something happens that the user can not control)
5) Predicate: What did the Subject do with the Object, e.g: Modified, Visited, Linked. Deleted, etc...

Zeitgeist tries to tackle this issue by logging, analysing and storing events.
To be continued...