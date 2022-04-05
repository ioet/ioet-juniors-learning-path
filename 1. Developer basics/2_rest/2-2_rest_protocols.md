# REST PROTOCOLS

## ¿ WHAT IS REST ?

REST is the acronym for REpresentational State Transfer, which is an architecture style that provides standards for communication between computer systems on the web in a simple way.
Currently, development platforms provide support to make use of web technologies, either through native or third-party frameworks or libraries, they also provide tools to process the information received in requests, whether these are XML, JSON or other types of data.
When REST was first raised, no specific protocol was established with which it should work, but due to the advances of the web and the great coupling with HTTP, this has become the main protocol used when thinking of REST, although it can be used in conjunction with other protocols such as SMTP, FTP or handle different types of data such as JSON or XML. [More information](https://learning.oreilly.com/library/view/rest-in-practice/9781449383312/ch01.html#technology_support)

## REQUESTS AND RESPONSES

When request a resource to the server, the type of content sent must be specified in the `content-type` field of the request header and it must be one of the options specified in the server's `accept`.

#### Example

Request

```rest
GET /articles/1 HTTP/1.1
Accept: text/html, application/xhtml
```

Response

```rest
HTTP/1.1 200 (OK)
Content-Type: text/html
```

### References

- O'Reilly Book: [RESTful Web APIs](https://learning.oreilly.com/library/view/restful-web-apis/9781449359713/)
- O'Reilly Book: [REST in Practice](https://learning.oreilly.com/library/view/rest-in-practice/9781449383312/)
- Article: [CodeAcademy - What is REST](https://www.codecademy.com/article/what-is-rest)
