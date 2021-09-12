# Code 301 - Read 07

In this file, a summary of **Read: Class 07 - REST** will be provided.

## REST

[GitHub post](https://gist.github.com/brookr/5977550)

* Who is Roy Fielding?

He is the person who helped writing the HTTP protocol for web servers that sent documents across the internet. Also, he did a lot of research explaining why the web works the way it does. His name is on the specification for the protocol that is used to get pages from servers to your browser.

* Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

> Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.

* What is the HTTP protocol that Fielding and his friends created?

It is a protocol that applies operations to machines using URLs. Examples:

1. When we go to a web page, the browser does an HTTP GET on the URL you typed in and back comes a web page.
2. Images in webpages are separate resources. The web page just specifies the URLs to the images and the browser does more GET requests using the HTTP protocol on them until all the resources are obtained and the web page is displayed.

* What does a GET do?

It allows systems to retrieve information from another system.

* What does a POST do?

It allows systems to add information to another system.

* What does PUT do?

It allows systems to replace something in another system.

* What does PATCH do?

It allows systems to partial update information on another system.
