# A beginner's guide to server-side rendering

The modern web has evolved over the years with new tools and technologies. We are introduced to new approaches to rendering websites and apps. With the rise of frameworks like NextJs and Remix, SSR has gained a lot of popularity in the last few years. i.e Server-side rendering. In this article, you will learn about what is SSR, how it works, and why you should care about it. So let's dive into it.

But before that let's understand what **rendering** means.

### 🎨 Rendering on the Web

In simple terms, rendering is a process of converting your code into something that users can see or interact with.

![rendering-diagram.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663605459915/tYjpKn6Uo.png align="left")

When you go to a website, the browser requests an HTML document from a server. The server returns the required file with all the linked resources. *Rendering is the process that combines all those resources to create a user interface in the browser.* Under the hood, it involves a lot of steps like parsing, building the DOM tree, CSSOM, Js compilation, painting, etc. You can read about it in detail [here](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work).

### 💻 Client-side rendering

To understand SSR well, let's have a quick look at Client side rendering first.

> Client-side rendering means rendering pages directly in the browser. All logic, data fetching, templating, and routing are handled on the client rather than the server.

![csr-111.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663608674025/UDP5Penqe.png align="center")

If you ever used react before, you might have noticed that the HTML file does not have any other content than a root `div`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671173052823/n2qw2hBwd.png align="center")

That's because React does the rendering on the client side. Once the bundled Js file is downloaded, it renders the website in the browser.

But as the application grows, the JavaScript required tends to grow as well resulting in more load time. Although, these can be fixed with techniques like code splitting and lazy loading. SSR solves this problem. Server-side rendering is a tool that can help you load your websites faster.

## 💡So what is Server side rendering?

SSR is one of the types of **pre-rendering**. Pre-rendering means the HTML is generated in advance, on a server, instead of having it all done by JavaScript on the user's device.

Server-Side Rendering renders the web pages on the server and then sends HTML files to the browser.

### 🪄 How it works

When a user visits a website, the server builds the webpage and sends a ready-made HTML file to the browser. All the processes like data fetching and templating are done on the server side before sending the response. The initial request loads the content as well. And the user interface is created.

![ssr-111.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1663608684274/TbaLFrnLA.png align="center")

After that React makes the components interactive (for example, attaching an event handler to a button). This process is also called **hydration**. In this way SSR lets users see the webpage before the JavaScript bundle loads and runs at the user end.

## 👍 Pros of SSR

*   Since a ready-made HTML is provided to the browser, It makes the initial load of the pages faster.
    
*   Server-side rendering is great for SEO. Your content is present before you get it. So search engines can index it and crawl it efficiently.
    
*   your site will be ranked higher in the search results if it is rendered on the server side. Google gives preferential search rankings to the sites with the fastest page load speed.
    
*   Fast-loading websites improve the user experience. Even if the user is running a slow internet connection or if the javascript is disabled on the browser, the application can be loaded.
    

## 👎 Cons of SSR

*   You're generally processing/rebuilding the same application multiple times - once on the client and once on the server. It can be costly and resource-intensive.
    
*   With server-side rendering, the browser displays the web page faster, but it still needs time to make it interactive. As a result, the app looks ready for interaction while the code is still being processed in the background. If the user tries to interact with the app during this period, there can be a delay in the browser’s response.
    
*   When the number of visitors increases on your site, with each user accessing a new page, it has to send a server request every time. Resulting in higher server costs.
    

## 🎯 Conclusion

Overall, server-side rendering has a good impact on SEO and performance. But CSR and SSR are not all black and white. Both have their pros and cons. And there are also hybrid options available that ensure the very first rendering of any page will happen from the server side only for the first time. Then all subsequent page requests will be CSR.

So when it comes to what should I choose, it mostly depends on the use case that fits your project.

### 📖 Further reading

*   [https://developer.mozilla.org/en-US/docs/Web/Performance/How\_browsers\_work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
    
*   [https://web.dev/rendering-on-the-web/](https://web.dev/rendering-on-the-web/)
    
*   [https://developer.mozilla.org/en-US/docs/Learn/Server-side/First\_steps/Introduction](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Introduction)