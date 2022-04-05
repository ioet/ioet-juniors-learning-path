## Topics

- [ALTERNATIVES TO REST](#alternatives-to-rest)
  - [SOAP](#soap)
      - [Example](#example)
  - [GRAPHQL](#graphql)
      - [Example](#example-1)
  - [FALCOR](#falcor)
      - [Example](#example-2)
    - [References](#references)

# ALTERNATIVES TO REST

## SOAP

Shortly, SOAP is XML. SOAP is a protocol that uses the XML specification for communication between the client and the server. It is a viable alternative to REST due to its robust and reliable architecture. A SOAP message is based on the syntax of XML `http://www.w3.org/2001/06/soap-envelope` namespace.

#### Example

```rest
<env:Envelope xmlns:env="http://www.w3.org/2001/09/soap-envelope">
  <env:Header>
    <n:note xmlns:n="http://example.org/note">
      <n:priority>1</n:priority>
      <n:expires>2021-12-10T14:00:00-05:00</n:expires>
    </n:note>
  </env:Header>Header>
  <env>Body>
    <m:alert xmlns:m="http://example.org/alert">
      <m:msg>Don't forget fill out Time Tracker</m:msg>
    </m:alert>
  </env>Body>
</env:Envelope>Envelope>
```

## GRAPHQL

GraphQL is a query language that serves as an agnostic transport of the protocols but is commonly used with HTTP. GraphQL provides a complete and understandable description of the data. It is not tied to any database or storage manager, so it can be attached to any project.

#### Example

```graphql
type User {
  id: ID
  name: String
}

function Query_me(request) {
  return request.auth.user;
}
```

## FALCOR

Falcor is a library for JavaScript, developed and maintained by Netflix, which allows abstracting the sources from which the data comes and representing them as a single domain model in a way that facilitates access and increases productivity by always having all the data available.

#### Example

```javascript
var falcor = require("falcor");
var model = new falcor.Model({
  cache: {
    todos: [
      {
        name: "get milk from corner store",
        done: false,
      },
      {
        name: "withdraw money from ATM",
        done: true,
      },
    ],
  },
});

// This returns:
// "get milk from corner store"
var name = await model.getValue("todos[0].name");
```

### References

- O'Reilly Book: [SOAP](https://learning.oreilly.com/library/view/programming-web-services/0596000952/ch02.html)

- O'Reilly Book: [FALCOR](https://netflix.github.io/falcor/)
