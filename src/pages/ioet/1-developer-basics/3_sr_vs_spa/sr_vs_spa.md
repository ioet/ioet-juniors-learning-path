---
layout: "../../../../layouts/BlogPost.astro"
title: "Server rendering vs single page apps"
---

## What are Single Page Applications ?

Single Page Applications are web pages that will work extraordinarily fast, even when navigating between different pages. The problem is that all this content will be available only after the JavaScript files finish loading. And this process can take many seconds.

These JavaScript files can be very heavy, since they take care of all the content and all the paths of our application. Fortunately, there are techniques such as Code Splitting that allow us to load the information of our application as users need it (for example, when browsing).

Even with these optimizations, the initial loading of SPAs is very slow. Users will not see content until they finish loading the JavaScript files. The advantage is that after waiting, the application runs at full speed.

Sometimes we also have to take care of authentication. Since we don't control the server, we have no way to verify if users are authenticated before they access the application. So we must use tokens (long live JSON Web Tokens!) to verify authentication every time we make requests to any server.

Many tools such as Create React App allow us to create Single Page Apps quickly and easily.

[![SPAl](https://i.ytimg.com/vi/6BozpmSjk-Y/maxresdefault.jpg)](https://youtu.be/6BozpmSjk-Y "SPA")

## What is Server Side Rendering ?

The applications that implement Server Side Rendering need (obligatorily) to configure their server, since this is the one in charge of "creating" an HTML file with all the data requested by the user in a specific path.

The initial load of each path is much shorter than in Single Page Applications. And there are also SEO benefits. But the process of loading and downloading information must be repeated every time users browse our application or must query new data.

Fortunately, we can create an application with SSR that becomes SPA when it reaches the client side. This is known as Progressive Server Side Rendering. In this way, both the initial loading and the navigation or user interactions will work extraordinarily fast.

On the authentication side we can also make fun combinations. We can take advantage of the moments where users reload or load the page for the first time. We store the authentication information in memory or in a database and track users to determine what their authentication status is.

Some tools like Next.js help us create applications using Server Side Rendering extremely quickly and easily. They have even evolved into FullStack programming frameworks (frontend and backend).

[![SSR](https://i.ytimg.com/vi/RAhYnK0v3rk/maxresdefault.jpg)](https://youtu.be/RAhYnK0v3rk "SSR")

## How SSRs Enhance Single Page Applications ?

A single page application, or SPA, is a type of web application that operates entirely from one page, usually with an “infinite scroll” user interface.

SPAs don’t require the entire page to reload when the end-user clicks or scrolls on a page element to fetch new data or to execute an action.

They’re built with Javascript and can be developed on a multitude of frameworks including Angular, Vue, and React.

Just like any other website, SPAs are accessed through a web browser. Still, the significant difference is that SPAs possess the ability to deliver more dynamic user experiences, and at a faster speed.

That being said, the UX of SPAs, especially in eCommerce sites, requires the content quickly and seamlessly. Also, SPAs SEO needs to be spot on for the website to rank

### Pros and Cons of SSRs for SPAs

**Pros**

- SEO friendly
- Users will see the content faster
- Shared code with backend node
- User-machine is less busy
- Best for static sites

**Cons**

- If your application is small, SSRs can improve performance. But if it’s heavy, it can degrade performance.
- SSRs increase response time if the server is busy.
- It can increase response size, ending with pages that take longer to load.
- SSRs increase the complexity of the application.

While the truth is that whether or not to build SPAs using SSR is context-dependent, server-side rendering can help you if your SPA is SEO-minded and needs to be fast and flexible to cope with your users’ needs.
