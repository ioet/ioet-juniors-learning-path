# Alternatives to REST

In this document you will find another alternatives to rest, specifically, we will focus on the following alternatives:

- GraphQL
- WebSockets
- gRPC

## Authors

- Jean Carlos Alarcón @jcalarcon98

## Topics

- [Alternatives to REST](#alternatives-to-rest)
  - [Authors](#authors)
  - [Topics](#topics)
  - [GraphQL](#graphql)
    - [Advantages](#advantages)
    - [Disadvantages](#disadvantages)
    - [A brief comparison with rest focusing in Data Fetching](#a-brief-comparison-with-rest-focusing-in-data-fetching)
    - [GraphQL - Additional Resources](#graphql---additional-resources)
  - [WebSockets](#websockets)
    - [When to use WebSocket?](#when-to-use-websocket)
    - [When not to use WebSocket?](#when-not-to-use-websocket)
    - [WebSockets - Additional Resources](#websockets---additional-resources)
  - [gRPC](#grpc)
    - [Characteristics](#characteristics)
    - [gRPC vs REST](#grpc-vs-rest)
    - [When to use gRPC?](#when-to-use-grpc)
    - [gRPC - Additional Resources](#grpc---additional-resources)

## [GraphQL](https://graphql.org/)

**GraphQL** is a modern alternative to rest created by Facebook in 2012. It is a query language for your APIs and a runtime for fulfilling those queries with your existing data. Provides a complete description of the data in your API. The most important feature of GraphQL is that it allows the client to ask for exactly what they need even in a single request.

GraphQL has three primary operations:

1. **Query** for reading data.
2. **Mutation** for writing data.
3. **Subscription** for automatically receiving real-time data.

### Advantages

- Good for complex systems and microservices.
- Fetching data with a single API call.
- No over/under fetching problems.
- Autogenerate API documentation.
- API evolution without versioning.
- Code-sharing.

### Disadvantages

- Web caching complexity.
- File uploading.
- Complex learning curve.

### A brief comparison with rest focusing in Data Fetching

Suppose you have to get the next time tracker information for a specific user:

- User
- User entries
- User projects

With a **REST API** you would typically retrieve the data by accessing multiple endpoints, for example you have to execute a [GET](2-1_http_verbs.md/#get) for each endpoint.

- GET /users/{id}
- GET /users/{id}/entries
- GET /users/{id}/projects

On the other hand, with GraphQL you would send a single query to the GraphQL server including the data you need, something like this:

```graphql
query getUser($id: Int){
  user(id: $id) {
    name,
    lastName,
    projects: {
      name
    },
    entries: {
      initDate,
      endDate
    }
  }
}
```

And the server will respond with a JSON objects, with all the information you have requested, everything in one only request.

### GraphQL - Additional Resources

- [GraphQL Official Page](https://graphql.org/)
- [GraphQL: Core Features, Architecture, Pros and Cons](https://www.altexsoft.com/blog/engineering/graphql-core-features-architecture-pros-and-cons/)
- [Why adopt GraphQL?](https://www.apollographql.com/docs/intro/benefits/)

## WebSockets

Websocket is a bidirectional communication protocol over a TCP connection. It is a stateful protocol, which means the connection between client and server will keep alive until it is terminated by either party (client or server). It can be used at the same time with REST apis.

### When to use WebSocket?

It can be used in application that require real-time communication, for example:

- Real-time web applications.
- Gaming Applications.

### When not to use WebSocket?

As you know, if we want real-time communication between client and server, go for WebSocket, but if we want to fetch old data, or if we want to get data only once to process it with an application, you should go with **HTTP protocol**.

### WebSockets - Additional Resources

- [WebSockets Official Doc](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)
- [Difference between HTTP and WebSocket](https://www.geeksforgeeks.org/what-is-web-socket-and-how-it-is-different-from-the-http/)

## [gRPC](https://github.com/grpc/grpc)

gRPC is a modern, open source, high-performance remote procedure call (RPC) framework developed by Google using **HTTP/2** that can run anywhere. gRPC enables client and server applications to communicate transparently, and simplifies the building of connected systems.

### Characteristics

- Highly efficient on wire and with a simple service definition framework.
- Simple service definition.
- Work across languages and platforms.
- Star quickly and scale.
- Bi-directional streaming and integrate auth.
- Easy to use.

### gRPC vs REST

| Features                     | gRPC                                                                                                                         | Rest                                                                                             |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **HTTP 1.1 vs HTTP 2**       | Follows a client-response model and is built on HTTP 2, which allows for: streaming communication and bidirectional support. | Follows a request-response model  and is typically built on HTTP 1.1.                            |
| **Browser Support**          | Limited browser support. gRPC requires gRPC-web and a proxy layer to perform conversions between HTTP 1.1 and HTTP 2.        | Universal browser support.                                                                       |
| **Payload Data Structure**   | gRPC uses Protocol Buffer by default to serialize payload data.                                                              | REST mainly relies on JSON or XML formats to send and receive data.                              |
| **Code Generation Features** | gRPC has native code generation features.                                                                                    | Developers must use a third-party tool like Swagger or Postman to produce code for API requests. |

### When to use gRPC?

**gRPC** architectural style has promising features that should be explored, for example:

- Efficiently connecting polyglot services in microservices style architecture.
- Connecting mobile devices, browser clients to backend services.
- Generating efficient client libraries.

### gRPC - Additional Resources

- [gRPC Official Page](https://grpc.io/)
