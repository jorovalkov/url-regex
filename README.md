URL-RegEx
=========

A Regular Expression for catching URLs and extracting fragments out of them.

``` javascript
RegEx = /\(?\b(?:(http|https|ftp):\/\/)?((?:www.)?[a-zA-Z0-9\-\.]+[\.][a-zA-Z]{2,4})(?::(\d*))?(?=[\s\/,\.\)])([\/]{1}[^\s\?]*[\/]{1})*(?:\/?([^\s\n\?\[\]\{\}\#]*(?:(?=\.)){1}|[^\s\n\?\[\]\{\}\.\#]*)?([\.]{1}[^\s\?\#]*)?)?(?:\?{1}([^\s\n\#\[\]\(\)]*))?([\#][^\s\n]*)?\)?/;
```

## How it works?

Match this RegEx against a chunk of text, and catch any URL inside it.
It should work on any programming language that supports Regular Expressions.

You can check [JavaScript example](http://someweblog.com/url-regular-expression-javascript-link-shortener/) of its use.

## URL fragments

It captures 8 groups (plus first group that contains entire URL). If some of them don’t exist in URL, that group will return empty.

1. Entire URL
2. Protocol
3. Domain
4. Port
5. Folders / Paths
6. Page / Filename
7. File extension
8. Parameters
9. Anchor
