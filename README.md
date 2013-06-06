URL-RegEx 1.2
=============

A Regular Expression for catching URLs and extracting fragments out of them.

``` javascript
RegEx = /\(?(?:(http|https|ftp):\/\/)?(?:((?:[^\W\s]|\.|[:]{1})+)@{1})?((?:www.)?(?:[^\W\s]|\.)+[\.][^\W\s]{2,4}|localhost(?=\/)|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(?::(\d*))?([\/]?[^\s\?]*[\/]{1})*(?:\/?([^\s\n\?\[\]\{\}\#]*(?:(?=\.)){1}|[^\s\n\?\[\]\{\}\.\#]*)?([\.]{1}[^\s\?\#]*)?)?(?:\?{1}([^\s\n\#\[\]]*))?([\#][^\s\n]*)?\)?/;
```

Match this RegEx against a chunk of text, and catch any URL inside it.
It should work on any programming language that supports Regular Expressions.

You can check [JavaScript example](http://someweblog.com/url-regular-expression-javascript-link-shortener/) of its use.

## URL fragments

It captures 8 groups (plus zero group that contains entire URL). If some of them don’t exist in URL, that group will return empty.

* **$0** - **Entire URL** - url being parsed
* **$1** - **Protocol** - http, https, ftp
* **$2** - **Userinfo** - username:password
* **$3** - **Domain** - www.mydomain.com, mydomain.com, 127.0.0.1, localhost...
* **$4** - **Port** - 80
* **$5** - **Path / Folders** - /folder/dir/
* **$6** - **Page / Filename** - eg. index
* **$7** - **File extension** - .html, .php...
* **$8** - **Query** - item=value&item2=value2
* **$9** - **Anchor** - #home
