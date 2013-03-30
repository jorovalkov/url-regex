URL-RegEx 1.0
=============

A Regular Expression for catching URLs and extracting fragments out of them.

``` javascript
RegEx = /\(?\b(?:(http|https|ftp):\/\/)?((?:www.)?[a-zA-Z0-9\-\.]+[\.][a-zA-Z]{2,4}|localhost(?=\/))(?::(\d*))?(?=[\s\/,\.\)])([\/]{1}[^\s\?]*[\/]{1})*(?:\/?([^\s\n\?\[\]\{\}\#]*(?:(?=\.)){1}|[^\s\n\?\[\]\{\}\.\#]*)?([\.]{1}[^\s\?\#]*)?)?(?:\?{1}([^\s\n\#\[\]\(\)]*))?([\#][^\s\n]*)?\)?/;
```

Match this RegEx against a chunk of text, and catch any URL inside it.
It should work on any programming language that supports Regular Expressions.

You can check [JavaScript example](http://someweblog.com/url-regular-expression-javascript-link-shortener/) of its use.

## URL fragments

It captures 8 groups (plus zero group that contains entire URL). If some of them don’t exist in URL, that group will return empty.

* **$0** - **Entire URL** - url being parsed
* **$1** - **Protocol** - http, https, ftp
* **$2** - **Domain** - www.mydomain.com, mydomain.com, localhost...
* **$3** - **Port** - 80
* **$4** - **Path / Folders** - /folder/dir/
* **$5** - **Page / Filename** - eg. index
* **$6** - **File extension** - .html, .php...
* **$7** - **Query** - item=value&item2=value2
* **$8** - **Anchor** - eg. #home
