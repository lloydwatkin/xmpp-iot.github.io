---
layout: article
title: "Friendship between peers"
categories: basics
modified: 2014-12-01T11:57:41-04:00
tags: [sample]
image:
  teaser: friends_image_400x250_white.png
toc: false
comments: false
ads: false
---


The most basic concept of using XMPP is the notion of 
friends. To exchange data between two endpoints they need to be
friends. The friendship is in reality to peers subscribing to one and
eachothers precense[^precense] updates.

[^precense]: Your state being *online*, *offline*, *available* etc 

##Friend request

The friending process starts with one end point asking another for a
"precense subscription" [Pidgin example][pidgin-ex]
The two enpoints can be in any domains **my-thing@my-domain.com/resource_id** makes a request to **your-thing@your-domain.com/**

##Confirm request

The enpoint confirms the request so now we have a single sided
subscription *my-thing* will recieve precense updates from
*your-thing*.  *your-thing* now sends a "precense subscription"
back to *my-thing* which inturn confirms the request. 

##Dual subscription

The two enpoints now have a dual subscription in talking to each other
so they can now send read and write. The information is stored on the
servers in the peer's rosters[^roster]

[^roster]: The storage of all your friends when you login and start a
new session the first thing you recieve is your roster, containing the
state of al your friend relations.

##Having a Parent, Adding security

The usage of friendship is very good if you are a human that can take your own descisions. But if we are a temp sensor we must talk to a trusted friend to ask for permissions.

Every device can have a "best friend" or "parent" which is the trusted party that takes the descisions regarding the device possibilities to respond to friendship requests and access to specific fields.

Using this way of endpoint security creates endless possibilities with
changing the ownership of devcices during first
commissioning[^commission] It can even support the usecase of
thirdparty delivering unnamed Things that you can buy in any store and then transfer them to be your own property

[^commission] The process when a Thing recieves it first configuration.

`JID (jabber id):` Every account in the XMPP network have an identity that looks like an email adress it is a uniqe identifier in the domain this is called the Jabber ID or **JID**. 
{: .notice-inverse}
`Resource:` For every login to a server a client will recive a **Resource** this id is used to distinguish between the different session. For example you being logged in to the same account from your *ipad*, *phone*, *computer* etc.
When working with Things it is seldom a Thing has several logins and resources but you should be aware of the possibility. 
{: .notice-inverse}

[pidgin-ex]: http://im.about.com/od/imfornewusers/ss/pidgin-account-adding-contacts.htm


