## HTTP Basics

The internet is a pretty complicated piece of technology, but luckily most of the complicated bits are handled for us automatically nowadays. Most data on the internet is sent using the `HTTP` protocol, which is what we'll focus on for this section.


### What is a Protocol?
A protocol is just a fancy word for an agreement between two groups on how they're going to communicate.  A famous example of a protocol would be Morse Code-- the code itself isn't super important, as long as everybody agrees on what the different symbols mean. HTTP is the main protocol used between computers on the internet-- it's an agreement on how messages should be sent back and forth.

### HTTP Basics
The HTTP protocol has two main parts: The `Request` and the `Response`. When you click on a link in your browser, your computer sends an HTTP `Request` to the server running the website. The server reads your request, decides what it should send back, and then sends you an HTTP `Response`.

An HTTP Request has these main parts:

**A Method**, which lets the server know what type of action you're requesting. When you click a link, the method is set to `GET`, because you want to GET some webpage from the server.
**A URI**, which is pretty much a fancy word for the URL of the page.
**Headers**, which contain information about your browser like what language you speak, what type of page you're asking for, the current time, etc... This information is useful for the server to understand what information to send back.
**A Body**, which is additional information sent with the request. This is usually data that you're sending to the server to post (for example, the content of a tweet that you want to send).

An HTTP response has most of the same information, but it doesn't have a URI or method. The Response also includes a `status code` to let the browser know what's going on. There's tons of different codes that all represent different things-- if you've ever seen a 404 error page, now you know where that number comes from!

Once your browser gets the response, it can read through it and display the webpage you asked for.


### HTTP Methods

The 2 main methods you need to worry about are `GET` and `POST`.  When you click on a link in your browser, you're sending a `GET` request to the server. This lets the server know you want it to send back some information. When you want to send new data to a server, your browser uses a `POST` request.  If you send a tweet, upload a profile picture, or leave a comment somewhere, a POST request is used. This lets the server know you would like to save *new*  data.

Although GET and POST are the most common types of request method, there's actually a lot more. If you're interested, here's a breakdown of what they all represent:


|Method|Description|
|-------|-------------|
|GET|Requests data from the specified location|
|POST|Sends data to be saved at the specified location|
|HEAD|Like GET, but asks for only headers to be sent back (no body)|
|PUT|Like POST, but asks to update data instead of creating new data|
|DELETE|Asks to delete data at the specified location|
|OPTIONS|Asks to get a list of allowed methods from the server |
|CONNECT|Asks the server to forward your request to another location |

Keep in mind that not every server will allow you to use all of these methods. Just because they exist doesn't mean that every website must accept them.


###Recommended Reading
[This](http://www.ntu.edu.sg/home/ehchua/programming/webprogramming/http_basics.html) article has a great overview of the HTTP protocol if you're interested in the specifics of how exactly it works. Don't worry if this is confusing-- most of this craziness is handled by the browser automatically.

[This](http://www.restapitutorial.com/httpstatuscodes.html) website has a great list of all the different status codes and what they represent.

[This](https://http.cat/) website a list of all the status codes along with corresponding cat pictures. It's not super helpful on the technical side of things, but it has cats.
