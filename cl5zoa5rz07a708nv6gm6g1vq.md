## How to build a performant and SEO-friendly websites

The most important part of building performant and SEO-friendly websites relies on our fundamental understanding of how websites work. Though at the presentation level, every website seems to function as same, certain websites have unique user experiences compared to others. Let's take the example of two well-known e-commerce websites Amazon and Flipkart. Though both the websites functionally deliver the same features and functionalities, the difference in the look and overall user experience is easier to notice even for general users. This is because Flipkart heavily relies on Client Side rendering but Amazon is more focused on Server Side Rendering.

Though both Amazon and Flipkart have server and client-rendered pages in their application. The balance between these two methods gives each its advantages and disadvantages.

### Rendering
In the context of websites, rendering is the process of building a presentable webpage that needs to be shown to the users. Based on the different approaches of how, when, and where we do the rendering process is the key to building performant and SEO-friendly web applications. Rendering methods can be closely correlated to different routing concepts. If you are not familiar with that, you can learn more about it from [here](https://johnpk.dev/routing-a-delusion-among-developers). The rendering process we will be discussing will be in the context of the user-defined process rather that a standard rendering process done by browsers. For more details on the standard rendering process of browsers refer to [this](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work). There are mainly three rendering approaches:

- Static Rendering
- Server Side Rendering
- Client Side Rendering

### Static Rendering
Statically Rendered webpages deliver ideal performance compared to other rendering methods and it is the benchmark that the other two methods strive to deliver. Generally, in static rendering, the webpages are prebuilt either manually or using static site generators like [Gatsby](https://www.gatsbyjs.com/) and [Eleventy](https://www.11ty.dev/). Since the webpages are prebuilt and there are no additional operations or functionality overhead that can cause website slowdown they proved to be an ideal way of rendering web applications whenever possible. But for large websites with millions of pages with dynamic content, this method would not be a feasible solution.

![static rendering.drawio.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658679545125/YQapJwKjq.png align="center")

#### Advantages
- **Fast and Performant** - No heavy lifting on both server and browser
- **SEO friendly** - Page contents are readily available for crawlers

#### Disadvantages
- **Difficult to develop and manage** - Without external static site generator tools managing static websites would be difficult
- **Code Redundancy** - Cannot leverage code reusability without external tools
- **High memory footprint** - As websites grow, static sites can become very big as there cannot share code across pages with similar layouts without the use of external tools

#### Ideal Use Cases
With the given advantages and disadvantages, static sites can be the go-to option for the below websites only if coupled with the right external tools such as [Eleventy](https://www.11ty.dev/) that makes development easier for developers
- Personal Blogging websites
- Documentation websites

### Server Side Rendering
Server-rendered websites generate the entire page dynamically in the server for each request from the users. Thus, it will be compute-intensive work for servers compared to the other two methods. Server-rendered websites leverage caching of website requests to a certain level but are not good enough to match the performance of statically rendered websites. Historically, Server-side rendering is the most predominantly used method.

![server rendering.drawio.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658684089683/b-fhp341F.png align="center")

#### Advantages
- **SEO Friendly**- Since the web pages are completely rendered on the server. Server-rendered websites are SEO friendly
- **Light Weight for Users** - As most of the process is done on the server. Server-rendered pages are less intensive on the user's device
- **Partial Rendering** - Just like videos, HTML is actually a stream that can be rendered by browsers as soon as it receives it. Server rendered application can leverage this to show the page contents to users even before completely loading the page thus improving [FCP](https://web.dev/fcp/) a critical performance factor
- **Developer Friendly** - Server-rendered websites can leverage code reusability and are highly customizable with the readily available tools and frameworks like Laravel, WordPress, etc

#### Disadvantages
- **High Cost** - Server-rendered applications can incur high costs since the server needs to do compute-intensive rendering tasks for every request
- **Scalability** - If not built as a stateless application, the server-rendered applications can be difficult for scaling to large audiences
- **Closely Coupled** - Since, both the frontend and backend application layers are closely coupled. It is will be difficult to migrate one without affecting another

#### Ideal Use Cases
With the given advantages and disadvantages, server-side rendering can be an ideal option for websites with millions of pages such as **E-commerce websites** and other websites where a slight delay in [FCP](https://web.dev/fcp/) has business impacting issues given that incurring additional costs does not outweigh that issue

### Client Side Rendering
The client-rendered application performs all the rendering processes on the user's device. Thus, this method is highly cost-efficient compared to server-rendered applications since the process which has been happening on the server is now distributed to the end users. Client-rendered websites are user-friendly since they leverage the browser's dynamic rendering capabilities to change page contents without a complete full page reload.

![client rendering.drawio.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1658687466144/Nsskh_Tm4.png align="center")

#### Advantages
- **User-friendly** - Though the initial load time is relatively high, the subsequent user experience is very good on client-rendered websites
- **DeCoupled** - Client-rendered websites are generally decoupled and are independent of the backend application thus making them highly flexible to manage
- **Ecosystem** - With the modernization of the front-end technologies, the front-end javascript libraries and frameworks made client-side rendering an ideal choice for developers to build and manage applications faster and easier

#### Disadvantages
- **Not SEO Friendly** - Client-rendered applications are generally bare-bone templates sent from the server. Thus making it a poor choice for building SEO-friendly websites
- **Initial Load Performace** - Since the rendering is done on is client-side via JavaScript, we cannot leverage the HTML streaming capabilities since the entire JavaScript needs to be loaded, parsed, and executed to render our application. This has a serious impact on [FCP](https://web.dev/fcp/)
- **Heavy for Users** - In order for the website to render completely, the additional dependencies should be loaded and processed on the end user's devices thus it affects the user's interactive time (also known as [TTI](https://web.dev/tti/)) based on the end user's device capabilities

#### Ideal Use Cases
With the given advantages and disadvantages, Client Side rendering is the most sought way of building modern applications due to its cost-effectiveness and subsequent website user experience. Most of the Web-based applications like GMail, Gsheets, etc are made possible only because of client-side rendering.

### A perfect method!
With all that covered, still, we cannot able to get all the goodness in one single method. A rendering method that is developer-friendly, user-friendly, SEO-friendly, performant, and cost-effective. This can be only achieved by using hybrid rendering methods where a single website can be capable of serving static pages, and server-rendered pages with the support for client-side rendering in the subsequent requests.

Such an approach comes with its own complexities and challenges which will be covered in my upcoming articles!

Feel free to share and post your comments!


