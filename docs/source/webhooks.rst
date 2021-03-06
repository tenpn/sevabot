============================================================
Sending Skype messages via webhooks
============================================================

.. contents:: :local:

Introduction
===============

Sevabot webhooks is a way to send Skype messages
from external services using HTTP GET and POST requests.

Because there is no "webhook" standard Sevabot supports different
ways to parse HTTP message payloads

* Signed and unsigned messages: shared secret MD5 signature prevents sending
  messages from hostile services

* HTTP GET and HTTP POST requests

* Service specific JSON payloads

To send a message to a chat you must first know to to the
id of a group chat. Sevabot server HTTP interface has a page
to show this list (see below).

Supported services and examples
============================================

Here are some services and examples how to integrate Sevabot

.. toctree::
   :maxdepth: 1

   bash
   zapier
   github
   subversion
   zabbix

Getting chat list
=======================

To send messages throught the bot you need to know

* Skype chat id - we use MD5 encoded ids to conveniently pass them in URLs.

* Sevabot shared secret in ``settings.py`` (only if your service supports MD5 signing, like your own custom shell script)

To get list of the chat ids visit in the Sevabot server hosted address::

    http://localhost:5000/

It will return a HTTP page containing a list of Sevabot internal chat ids.







