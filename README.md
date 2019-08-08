# NodeJS
Learnt Notes for NodeJS
Node JS is a runtime enviroment for executing JavaScript code outside a browser.
This can be 
-> Desktop Apps
-> Servers
-> Anything else you want to run with JavaScript
-> back-end services such as API (Application Programming Interface)
*/
Node is not a programming a language and not be compared to ASP.NET, rails or Django (as Node is not a framework). It is a runtime....

Web App or Mobile App are dependent and talk to back-end service or in the cloud. This may be to store data, send emails or push notifications. 
Node is ideal for highly-scalable, data-intensive and real-time apps

How does this compete with the likes of Rails and Django?
Node is easy to get started, for prototyping and agile development, superfast and highly scalable.
Node applications use JavaScript. JavaScipt is a more cleaner and more consistent codebase.
Large ecosystem of open-source libs. 

Architecture of Node JS:

Before Node
JavaScript was only used to build applications that run inside a browser[is a runtime enviroment]. Every browser had a JS Engine, that took JS Code and converted it into machine code.
Microsoft Edge uses Chakra. Safari uses SpiderMonkey and Google uses v8. Due to these variety of engines, sometimes Javascript code behave differently in browser or another. 
In 2009. Ryan Dahl took Google's v8 engine, which is the fastest JS engine out there and embedded it inside a C++ Program, called Node.exe.

So similar to a browser, node is a runtime enviroment for Javascript code, containing additional modules that give us capabilities not available inside a browser browser. e.g. fs.readFile() or http.createServer.

Highly scalable due to the non-blocking/asynchronous architecture. A single thread can handle multiple requests. Upon a request, a thread is allocated to handle that request. It is likely to query a database and may time until the result is ready. While a thread is waiting, it cannot be used to handle another request, so instead another new thread is allocated. 

Eventually, when dealing with a large number of concurrent clients, we will run of threads. Hence clients will either have to wait or, we allocate more hardware. So with this architecture, we aren't allocation our resources probably. This is the problem with blocking/asynchrous architecure. 

Node applications are asynchrous by default. A Single thread is used to handle all requests, no waiting. A query can be used to handle multiple clients. When the result is ready, a message is pushed into the EventQueue, that is currently being monitored in the background. When an event is ready, it is taken out and processed. Node should not be used for CPU-intensive apps. 
