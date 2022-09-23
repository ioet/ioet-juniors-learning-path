---
layout: "../../../../layouts/BlogPost.astro"
title: "HTTP VERBS"
pubDate: "2022-09-14"
---

The protocol HTTP defines a set of request methods, which are also called verbs.

- [HEAD](#head)
  - [Syntax](#syntax)
  - [Common Status Responses](#common-status-responses)
- [GET](#get)
  - [Syntax](#syntax-1)
  - [Common Status Responses](#common-status-responses-1)
- [POST](#post)
  - [Syntax](#syntax-2)
  - [Common Status Responses](#common-status-responses-2)
- [PUT](#put)
  - [Syntax](#syntax-3)
  - [Common Status Responses](#common-status-responses-3)
- [PATCH](#patch)
  - [Syntax](#syntax-4)
  - [Common Status Responses](#common-status-responses-4)
- [DELETE](#delete)
  - [Syntax](#syntax-5)
  - [Common Status Responses](#common-status-responses-5)
- [OPTIONS](#options)
  - [Syntax](#syntax-6)
  - [Common Status Responses](#common-status-responses-6)
- [CONNECT](#connect)
  - [Syntax](#syntax-7)
  - [Common Status Responses](#common-status-responses-7)
- [TRACE](#trace)
  - [Syntax](#syntax-8)
  - [Common Status Responses](#common-status-responses-8)
- [References](#references)

## HEAD

The HEAD method performs the action of requesting data to receive the headers of the resource.

### Syntax

```rest
HEAD /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## GET

The GET method, as well as HEAD, are considered safe methods, for this reason they should not perform any action other than receiving information. The GET method allows making requests to the server waiting to receive the requested resource.

### Syntax

```rest
GET /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## POST

The POST method sends data to the server with a type of body indicated by Content-Type header. When information is sent using a form, there are several types of encryption of the information that can be used, among others, the following can be listed:

- application/x-www-form-urlencoded
- multipart/form-data
- text/plain

### Syntax

```rest
POST /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 201  | CREATED     |
| 404  | NOT FOUND   |
| 409  | CONFLICT    |

## PUT

The PUT method sends a payload to a target resource so that it can be modified if it exists.

### Syntax

```rest
PUT /index.html
```

### Common Status Responses

| Code | Description       |
| ---- | ----------------- |
| 200  | OK                |
| 204  | NO CONTENT        |
| 301  | MOVED PERMANENTLY |
| 404  | NOT FOUND         |

## PATCH

The PATCH method performs the same function of the PUT method with the difference that PATCH should be used when it is required to modify the information of the target resource in a partial way.

### Syntax

```rest
PATCH /index.html
```

### Common Status Responses

| Code | Description       |
| ---- | ----------------- |
| 200  | OK                |
| 204  | NO CONTENT        |
| 301  | MOVED PERMANENTLY |
| 404  | NOT FOUND         |

## DELETE

The DELETE method requests the server to delete the target resource. The functionality of this request may be modified by the rules or policies of whoever administers the request, so the client cannot ensure that when executing this request, the resource will be deleted from the target servers.

### Syntax

```
DELETE /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## OPTIONS

The OPTIONS method requests information about the communication options available with the target resource, this method can also include a body in the request.

### Syntax

```rest
OPTIONS /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## CONNECT

The CONNECT method allows establishing a two-way communication to the target resource, establishing this connection through a tunnel.

### Syntax

```rest
CONNECT /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## TRACE

The TRACE method performs a loopback test message to the target resource.

### Syntax

```rest
TRACE /index.html
```

### Common Status Responses

| Code | Description |
| ---- | ----------- |
| 200  | OK          |
| 404  | NOT FOUND   |

## References

For more information, you can visit:

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
- [MDN Web Docs - HTTP Response Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
- [W3](https://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html)
