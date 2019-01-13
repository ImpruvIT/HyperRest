# HyperRest
Simple .Net Standard based library for formatting and parsing of hyperlink RESTful documents.

## Motivation
Why another RESTful formatter is needed? I needed a simple HAL response parser and I did not like any of [these](https://github.com/mikekelly/hal_specification/wiki/Libraries#c-sharp). Most are clients handling also HTTP communication. Others does not handle CURIEs transparaently and let applications code to handle it.

As a result I decided to design and implement a new library with following goals:
 - Pure formatter and parser - no handling of an HTTP communication
 - No dependency of application model on library - hyperlink document uses composition of application model instead of inheritance
 - Domain model of hyperlink document is independent of representation - same hyperlink document can be formatted using different representations (although only HAL is planned to be implemented at the moment)
 - Domain model of hyperlink document is independent of serialization - same hyperlink document can be formatted using different serializers (although only JSON is planned to be implemented at the moment)
 - Transparent handling of CURIEs - the application using this library does not concern about whether CURIEs are used at all or which prefix is used
