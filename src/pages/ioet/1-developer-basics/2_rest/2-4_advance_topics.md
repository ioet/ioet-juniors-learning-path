---
layout: "../../../../layouts/BlogPost.astro"
title: "Recipes to build a REST API"
pubDate: "2022-09-14"
---
In this document you will find some interesting guidelines to be more effective at building a REST API

## Contributors

- [Jipson Murillo](https://github.com/Jobzi)
- [Wladymir Brborich](https://github.com/Wason1797)

## Content

- [Contributors](#contributors)
- [Content](#content)
- [API Error format](#api-error-format)
  - [Internal Server Errors](#internal-server-errors)
  - [When should we return 4xx or 5xx status codes to the client?](#when-should-we-return-4xx-or-5xx-status-codes-to-the-client)
- [Self-generated documentation](#self-generated-documentation)
  - [Why ?](#why-)
- [When should we use PUT and when should we use POST?](#when-should-we-use-put-and-when-should-we-use-post)
  - [Caveats](#caveats)
- [When should we use the PATCH HTTP method?](#when-should-we-use-the-patch-http-method)
  - [Caveats](#caveats-1)
- [What are idempotent and/or safe methods?](#what-are-idempotent-andor-safe-methods)
- [Idempotent methods](#idempotent-methods)
- [Pagination](#pagination)
- [Async Operation](#async-operation)
- [More Topics](#more-topics)

## API Error format

My API returns errors in various cases:

- the request does not satisfy my business rules
- a resource does not exist
- the request is not properly formatted
- an unexpected error occurred (yes, it happens!)

In case of an error, I already know about [HTTP status codes](https://httpstatuses.com/) (should be in `4xx` or `5xx`), but what should I put in the response body?

**Choose an error format for your API, and stick with it.**

The error response body should be an object, containing always the same attributes.

It should at least contain:

- an **error code**: a human-readable code, shortly describing the problem, usable by an application to identify the error.
  - the error code is unique for each error case.
  - a Client (like a frontend) may be able to write a condition on this code, for example to display a specific message to the user.
  - suggested format: upper snake case, with explicit words
  - e.g.: `PRODUCT_NOT_FOUND`, `ORDER_ALREADY_PAID`, `NO_SEARCH_RESULT`...
- an **error message**: a human-readable description, fully describing the problem.
  - the message may differ from one occurrence to another: it can contain data explaining this specific error, eg: `The product #42 is no longer available.`
  - this message is meant for helping Client developers to debug. In most cases, it should not be displayed as is to an end-user.

The complete format depends on your API standard (snake or caml case, etc.). Here is a suggestion:

```json
{
  "error_code": "PRODUCT_NOT_FOUND",
  "error_message": "The product #42 is no longer available."
}
```

[Read more](link)

### Internal Server Errors

Unexpected exceptions should always be caught at the higher level of your application, so that they are transformed to a [500 API error](https://httpstatuses.com/500) with a neutral message.

For security concerns, always avoid to expose your implementation details in your API responses (stack trace, database errors, etc.).\
Use logs instead for debugging the error.

Here is a suggestion of a response body for a 500 error:

```json
{
  "error_code": "UNEXPECTED_ERROR",
  "error_message": "An unexpected error occurred."
}
```

[Read more](https://octo-woapi.github.io/cookbook/error-format.html)

### When should we return 4xx or 5xx status codes to the client?

4xx codes are used to tell the client that a fault has taken place on THEIR side. They should not retransmit the same request again, but fix the error first.

5xx codes tell the client something happened on the server and their request by itself was perfectly valid. The client can continue and try again with the request without modification.

If your API is trying to save a record to a database and this fails because there is an error with the database, for instance, it's not reachable, or a constraint fails, use a 5xx code (preferably 500 - Internal server error). Always add a response to what went wrong. This response SHOULD be displayed to the client, or if it's an automated system, it can retry again with the same request.

If you as a client receive a 500 status code, you can decide to try again (after a waiting-period, for a set number of times) to see if the server can handle the same request later on. Some status codes like 503 can return a retry-after header. This can be used to figure out how long a client SHOULD wait until a next attempt should be tried.

## Self-generated documentation

My e-commerce API exposes products.\
I want to use self-generated documentation to:

- Facilitate the integration of an API
- Document effectively

### Why ?

When building a REST API, we design an API that can be used by external developers and users. Documentation is a concise reference manual containing all the information required to work with the API.

- API documentation improves the experience for developers and users.
- Serve as a guide to help users become familiar with the API.
- Increases adoption rate.
- Documentation is the key to a good experience when consuming your API.
- Reduces onboarding time.
  See More: [Self-generated documentation](https://octo-woapi.github.io/cookbook/self-generated-documentation.html)

## When should we use PUT and when should we use POST?

The HTTP methods POST and PUT aren't the HTTP equivalent of the CRUD's create and update. They both serve a different purpose. It's quite possible, valid and even preferred in some occasions, to use PUT to create resources, or use POST to update resources.

Use PUT when you can update a resource completely through a specific resource. For instance, if you know that an article resides at <http://example.org/article/1234>, you can PUT a new resource representation of this article directly through a PUT on this URL.

If you do not know the actual resource location, for instance, when you add a new article, but do not have any idea where to store it, you can POST it to an URL, and let the server decide the actual URL.

```rest
PUT /article/1234 HTTP/1.1
<article>
    <title>red stapler</title>
    <price currency="eur">12.50</price>
</article>
```

```rest
POST /articles HTTP/1.1
<article>
    <title>blue stapler</title>
    <price currency="eur">7.50</price>
</article>

HTTP/1.1 201 Created
Location: /articles/63636
```

### Caveats

PUT and POST are both unsafe methods. However, PUT is idempotent, while POST is not.

## When should we use the PATCH HTTP method?

The HTTP methods PATCH can be used to update partial resources. For instance, when you only need to update one field of the resource, PUTting a complete resource representation might be cumbersome and utilizes more bandwidth.

Also, the PUT method is idempotent. PUTting the same data multiple times to the same resource, should not result in different resources, while POSTing to the same resource can result in the creation of multiple resources.

```rest
PATCH /user/jthijssen HTTP/1.1
<user>
    <firstname>Joshua</firstname>
</user>
```

### Caveats

PATCH is neither safe nor idempotent.
An API implementing PATCH must patch atomically. It MUST not be possible that resources are half-patched when requested by a GET.

## What are idempotent and/or safe methods?

Safe methods are HTTP methods that do not modify resources. For instance, using GET or HEAD on a resource URL, should NEVER change the resource. However, this is not completely true. It means: it won't change the resource representation. It is still possible, that safe methods do change things on a server or resource, but this should not reflect in a different representation.

```rest
GET /blog/1234/delete HTTP/1.1
```

Safe methods are methods that can be cached, prefetched without any repercussions to the resource.

## Idempotent methods

An idempotent HTTP method is a HTTP method that can be called many times without different outcomes. It would not matter if the method is called only once, or ten times over. The result should be the same. Again, this only applies to the result, not the resource itself. This still can be manipulated (like an update-timestamp, provided this information is not shared in the (current) resource representation.

Idempotency is important in building a fault-tolerant API. Suppose a client wants to update a resource through POST. Since POST is not a idempotent method, calling it multiple times can result in wrong updates. What would happen if you sent out the POST request to the server, but you get a timeout. Is the resource actually updated? Does the timeout happened during sending the request to the server, or the response to the client? Can we safely retry again, or do we need to figure out first what has happened with the resource? By using idempotent methods, we do not have to answer this question, but we can safely resend the request until we actually get a response back from the server.

[Read More](https://restcookbook.com/HTTP%20Methods/idempotency/)

## Pagination

Pagination is an important part of building an API. Often times you need to return large ammounts of information to the client. In some cases this can lead to problems, in which your endpoint cannot handle the load, or the client does not have enough memory to store the payload.

Pagination prevents this by splitting the payload in chunks, and giving the client a clear indication on how to fetch the next part of the payload.

Often times, pagination should be implemented at the database level, to optimize query performance. Search for implementations in your ORM of choice or design your SQL queries arround it.

[Read More](https://restcookbook.com/Resources/pagination/)

## Async Operation

Asynchronous APIs aim to solve issues with having to wait a resource to be processed for to long. This in itself is a large topic that requires much depth. But if you want some guidelines in how to correctly implement REST into your async API you can read more [here](https://restcookbook.com/Resources/asynchroneous-operations/)

## More Topics

- [Batch Processing](https://octo-woapi.github.io/cookbook/batch-processing.html)
- [Internationalization](https://octo-woapi.github.io/cookbook/internationalization.html)
