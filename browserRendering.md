# Browser rendering

The structure of a web page is made using _HTML_, which consists of several tags for specific purposes. These tags/elements are wrapped up within a **document** object, which represents the entire hierarchy of our HTML code structure.
Similarly, the CSS code is converted into CSSOM i.e. _CSS object model_

It was important to be aware of this because it plays a vital role in understanding the mechanism involved in rendering a HTML, CSS page.

### The step-wise process is as follows

- **Fetching Data**
The web page is fetched over hypertext transfer protocol(HTTP). Since the machine only understands data in bit 0 or 1. The data is fetched into bytes which further is converted into HTML characters based on HTML encoding standards. The same happens to CSS files. Keep in mind, that the browser may send multiple requests to fetch any external file (if included), apart from plain HTML code.
<br>

- **Parsing Data**
The characters that are formed in the above step still don't make sense to the computer. Hence, it is further parsed into a document object model. Top of the hierarchy is the document object which contains HTML tags as nodes in its structure which are accessible using the document object. Similarly, the CSS file is converted into a CSS object model
<br>

- **Render Tree formation**
After both DOM and CSSOM are created. Browser does combine both structures into a render tree. The render tree is nothing but information of all the nodes as the browser should know where a particular thing has to be rendered once we make the final layout.
<br>

- **Making layout**
Meanwhile making the render tree, it stored all the information about the position/size of each node in DOM. So, we move on to make the final layout of the page that has to be rendered.
<br>

- **Painting**
The layout is ready. Also, we had the information on its styling as per CSSOM. And it paints the nodes in our DOM one by one.
<br>

- **Final Composition and rendering**
The final step includes combining all painted layers and rendering everything on the screen optimally.
<br>

<sub>*DOM Tree*</sub>

![DOM Tree](domVisual.gif)
<br>

`Point to remember: If there is JavaScript linked to your HTML page as well, it will perform its action on DOM before the page is rendered. The reason we should use the script tag at the end of the body is that DOM construction is stopped once the browser finds the script tag and gives priority to executing the script first.`

### References

[How browser rendering works — behind the scenes](https://blog.logrocket.com/how-browser-rendering-works-behind-scenes/)

[Quora- How browsers render CSS/html](https://www.quora.com/How-do-browsers-render-HTML-CSS)

[Blog](https://starkie.dev/blog/how-a-browser-renders-a-web-page)

