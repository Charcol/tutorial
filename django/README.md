# What is Django?

Django (_/ˈdʒæŋɡoʊ/ jang-goh_) is a free and open source web application framework, written in Python. It's a web framework - a set of components that helps you to develop websites faster and easier.

You see, when you're building a website, you always need a similiar set of components: a way to handle user authentication (signing up, signing in, signing out), management panel for your website, forms, uploading files, etc.

Luckily for you other people long ago noticed that web developers face similar problems when building a new site, so they teamed up and created frameworks (Django is one of them) that give you ready components you can use.

Frameworks exist to save you from having to reinvent the wheel and help alleviate some of the overhead when you’re building a new site.

## Why do you need a framework?

To understand what Django actually is for, we need a closer look at the servers. The first thing is that the server needs to know that you want it to serve you a webpage.

Imagine a mailbox (port) which is monitored for incoming letters (requests). This is done by a web server. The web server reads the letter, and sends a response with a webpage. But when you want to send something, you need to have some content. And Django is something that helps you create the content.

## What happens when someone requests a website from your server?

When a request comes to a web server it's passed to Django which tries to figure out what actually is requested. It takes a webpage address first and tries to figure out what to do. This part is done by Django's __urlresolver__ (Note that a website address is called a URL - Uniform Resource Locator, so the name *urlresolver* makes sense). It is not very smart - it takes a list of patterns and tries to match the URL. Django checks patterns from top to the bottom and if something is matched then Django passes the request to the associated function (which is called *view*).

Imagine a postman with a letter. She is walking down the street and checks each house number with the one on the letter. If it matches, they put the letter there. This is how the urlresolver works!

In the *view* function all interesting things are done: we can look at a database to look for some information. Maybe the user asked to change something in the data? Like a letter saying "Please change description of my job." - the *view* can check if you are allowed to do that, then update the job description for you and send back a message: "Done!". Then the *view* generates a response and Django can send it to the user's web browser.

Of course, the description above is a little bit simplified, but you don't need to know all the technical things yet. Having a general idea is enough.

So instead of diving too much into details, we will simply start creating something with Django and we will learn all the important parts along the way!


