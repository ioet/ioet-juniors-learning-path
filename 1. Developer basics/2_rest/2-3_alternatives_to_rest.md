# ALTERNATIVES TO REST
## [SOAP](https://learning.oreilly.com/library/view/programming-web-services/0596000952/ch02.html)
Shortly, SOAP is XML. SOAP is a protocol that uses the XML specification for communication between the client and the server. It is a viable alternative to REST due to its robust and reliable architecture. A SOAP message is based on the syntax of XML `http://www.w3.org/2001/06/soap-envelope` namespace.

#### Example

<pre style="background-color: #F4F4F4; border-left: 6px solid #5EBAE9;">
&lt;env:Envelope xmlns:env="http://www.w3.org/2001/09/soap-envelope"&gt;
  &lt;env:Header&gt;
    &lt;n:note xmlns:n="http://example.org/note"&gt;
      &lt;n:priority&gt;1&lt;/n:priority&gt;
      &lt;n:expires&gt;2021-12-10T14:00:00-05:00&lt;/n:expires&gt;
    &lt;/n:note&gt;
  &lt;/env:Header&gt;
  &lt;env:Body&gt;
    &lt;m:alert xmlns:m="http://example.org/alert"&gt;
      &lt;m:msg&gt;Don't forget fill out Time Tracker&lt;/m:msg&gt;
    &lt;/m:alert&gt;
  &lt;/env:Body&gt;
&lt;/env:Envelope&gt;
</pre>


## [GRAPHQL](https://graphql.org/learn/)
GraphQL is a query language that serves as an agnostic transport of the protocols but is commonly used with HTTP. GraphQL provides a complete and understandable description of the data. It is not tied to any database or storage manager, so it can be attached to any project.

#### Example

<pre style="background-color: #F4F4F4; border-left: 6px solid #5EBAE9;">

type User {
  id: ID
  name: String
}

function Query_me(request) {
  return request.auth.user;
}
</pre>

## [FALCOR](https://netflix.github.io/falcor/)

Falcor is a library for JavaScript, developed and maintained by Netflix, which allows abstracting the sources from which the data comes and representing them as a single domain model in a way that facilitates access and increases productivity by always having all the data available.

#### Example

<pre style="background-color: #F4F4F4; border-left: 6px solid #5EBAE9;">

var falcor = require('falcor');
var model = new falcor.Model({
    cache: {
        todos: [
            {
                name: 'get milk from corner store',
                done: false
            },
            {
                name: 'withdraw money from ATM',
                done: true
            }
        ]
    }
});

// This returns:
// "get milk from corner store"
var name = await model.getValue('todos[0].name');
</pre>
