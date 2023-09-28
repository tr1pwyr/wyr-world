---
title: Web Forms
date: 2023-05-20
status: publish
permalink: /web-forms
author: Tr1pWyr
description: The humble webform, it may seem like a simple thing, it is the backbone of the internet.
id: 3793
thumbnail: /uploads/images/web-forms.webp
category:
    - Technology
tags:
    - 'web forms'
    - 'webform'
    - html
---

There are no little components...

# The Humble Web Form

> Consider the humble webform, while it may seem like a simple thing, it is the backbone of the internet. Every time you fill out a contact form, sign up for a newsletter, or make a purchase online, you are using a web form. Web forms are used for everything from collecting customer information to processing payments. 

![Web Forms](/uploads/images/web-forms.webp)

HTML forms have played a pivotal role in shaping the interactive nature of the World Wide Web, providing users with a means to input and submit data on web pages. Their history can be traced back to the early days of the web when Tim Berners-Lee first conceived the idea of the World Wide Web in the late 1980s. Initially, web pages were static and could only display information. There was no way for users to interact with web content beyond clicking on hyperlinks.

## HTML Forms

The breakthrough came in 1993 when a researcher at the European Organization for Nuclear Research (CERN), Dave Raggett, proposed the concept of HTML+ (HTML Plus). This extension to the existing HTML markup language introduced the "FORM" element, which allowed users to create interactive forms on web pages. These forms could include input fields, checkboxes, radio buttons, and buttons to submit data to a server. 

Soon after, [Marc Andreessen](https://en.wikipedia.org/wiki/Marc_Andreessen) and Eric Bina created the Mosaic web browser, which implemented support for HTML forms, making them accessible to a broader audience. This innovation laid the foundation for the dynamic and transactional nature of the modern web, enabling e-commerce, online surveys, and various other interactive web applications to flourish. 

![Web Forms](/uploads/images/web-forms-2.webp)

Since then, HTML forms have evolved with new elements and attributes, but their fundamental purpose of collecting and transmitting user data remains a core component of web development.
The most common use of the web form is as a way to contact a website's owner. This brings up the issue of what do you do when a contact form is submitted? Traditionally contact forms sent a website admin an email. Maybe the form's content is also added to a contacts database.

### Web Forms and Email

HTML Forms with tradition input submit made sense back when websites ran on machines that also ran mail servers, before everyone went SMS, etc. These days whether you are deploying to the GCP, Linode, CloudFlare Pages, etc. running a mail server in a pain is the ass.

I've approached this in a number of different ways:

- Firebase functions
- [MailGun](https://www.mailgun.com/)
- Actual SMTP Mail Server
- 3rd Party Form End Points

Each has its pluses and minuses.

If you are using the [GCP Firebase](https://firebase.google.com/firebase-and-gcp) functions are awesome. They are also overkill for a simple contact form. If you want to database your form submissions, perform some logic on the submission, etc. then Firebase Functions might be the way to go. Keep in mind that Firebase Functions include a good deal of overhead and will increase the size of your project.

Mailgun and similar services provide what I think of as virtual mail servers. You can send the content of your webform to the Mailgun API and choose what happens next. You will need to update MX records to choose this option.

If you are scared of [MX records](https://mxtoolbox.com/) you are free to completely skip this section. Running a mail server is no joke. Even admins that know all the ins and outs of a web server can get tripped up trying to configure a mail server. Even if you do get it set up you have to make sure other mail servers trust it. It is an expensive solution as well.
Form Endpoints

That brings us to the fourth option - third party endpoints. These are services that provide APIs that you can send your form data to. Basically you are subcontracting handling form data to a third party. I had no idea how many services like this exist. There are three that I can recommend: FormKeep (formerly Formcake)

I like [Formkeep](https://formkeep.com/) the best out of all web form services that I have tried so far. I signed up for the paid dev plan after my testing phase - in fact I am using it for the contact me for this site. The other 3 services that I have tried and that work as advertised are Formspree, 99Inbound and Formcarry. I would like to recommend Form.taxi but in my case it took hours for the submissions to show up. 

