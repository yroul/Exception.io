Exception.io: JavaScript
========================

A collection of custom exception classes written in JavaScript.

## Inheritance Hierarchy

    Error
    └── Exception
        ├── ArgumentException
        ├── InvalidInputException
        ├── NotImplementedException
        ├── NotSupportedException
        ├── NotFoundException
        ├── UnauthenticatedException
        └── UnauthorizedException

## Classes

<table>
  <thead>
    <tr><th>Class Name</th><th>Description</th><th>Default Message</th></tr>
  </thead>
  <tbody>
    <tr><td>Exception</td><td>The exception that is thrown when an error occurs.</td><td>No Description</td></tr>
    <tr><td>ArgumentException</td><td>The exception that is thrown when one of the arguments provided to a method is not valid.</td><td>Invalid Argument</td></tr>
    <tr><td>InvalidInputException</td><td>The exception that is thrown when one of the input provided to a method is not valid.</td><td>Invalid Input</td></tr>
    <tr><td>NotImplementedException</td><td>The exception that is thrown when a requested method or operation is not implemented.</td><td>Not Implemented</td></tr>
    <tr><td>NotSupportedException</td><td>The exception that is thrown when a requested method or operation is not supported.</td><td>Not Supported</td></tr>
    <tr><td>NotFoundException</td><td>The exception that is thrown when an attempt is made to find something that does not exist.</td><td>Not Found</td></tr>
    <tr><td>UnauthenticatedException</td><td>The exception that is thrown when a requested method or operation requires authentication.</td><td>Not Authenticated</td></tr>
    <tr><td>UnauthorizedException</td><td>The exception that is thrown when the current user is not allowed to perform an attempted operation.</td><td>Not Authorized</td></tr>
  </tbody>
</table>

## Usage
Initiate any one of the exception classes.

    if (item == null) {
        throw new NotFoundException("Item not found.");
    }

Check the type of exception we are dealing with:

    var err = new Exception();

    err instanceof Exception               // → true
    err instanceof Error                   // → true
    Exception.prototype.isPrototypeOf(err) // → true
    Error.prototype.isPrototypeOf(err)     // → true
    err.constructor.name                   // → "Exception"
    err.name                               // → "Exception"
    err.message                            // → "No description"
    err.toString()                         // → "[Exception] No description"
    err.stack                              // → prints the stack trace

Handle specific exception types using exception's constructor property:

    try {
      foo("valA", "valB");
    }
    catch (e) {
      if (e instanceof ArgumentException) {
        console.error(e.toString());
      }
      else if (e instanceof InvalidInputException) {
        console.error(e.toString());
      }
      else {
        console.error(e.toString());
      }
    }

## Supported Platforms
- Web Browsers
- [Node.js](http://nodejs.org)
- [Titanium](http://www.appcelerator.com/platform/titanium-platform)
- [Cordova](http://cordova.apache.org) (formerly [PhoneGap](http://phonegap.com))

## Contributors
- [Zeeshan Mian](http://zmian.me)

## License

(The MIT License)

Copyright (c) 2013 Zeeshan Mian

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
