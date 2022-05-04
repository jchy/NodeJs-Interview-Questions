# NodeJs-Interview-Questions

Q. Give an example where call apply bind is. Required?
( https://betterprogramming.pub/when-to-use-bind-call-and-apply-in-javascript-1ae9d7fa66d5 )

Q. What is curl ?
curl -X POST --header "Content-Type:application/json" -d "{\"title\": \"Developer Jaswant\",\"body\":\"Software Engineer\"}" https://jsonplaceholder.typicode.com/posts

curl --data "title=Jaswant&body=Hello it's me" https://jsonplaceholder.typicode.com/posts

curl -o data.txt --data "title=Jaswant&body=Hello it's me" https://jsonplaceholder.typicode.com/posts

Q. What is the difference between readFile and readFileSync?
Ans. In fs. readFile() method, we can read a file in a non-blocking asynchronous way, but in fs. readFileSync() method, we can read files in a synchronous way, i.e. we are telling nodes.

You need to show your readFileSync code if you're not simply replacing readFile with readFileSync.

Also, just so you're aware, you should never call readFileSync in a node express/web server since it will tie up the single thread loop while I/O is performed. You want the node loop to process other requests until the I/O completes and your callback handling code can run.

Q. What does process in node.js mean?
Ans. The process object in Node. js is a global object that can be accessed inside any module without requiring it. There are very few global objects or properties provided in Node. js and process is one of them. It is an essential component in the Node.



Q. What is Node.js? Where can you use it?
Ans. Node.js is an open-source, cross-platform JavaScript runtime environment and library to run web applications outside the client’s browser. It is used to create server-side web applications.

Node.js is perfect for data-intensive applications as it uses an asynchronous, event-driven model. You can use  I/O intensive web applications like video streaming sites. You can also use it for developing: Real-time web applications, Network applications.

Cross-platform: developing software products for multiple platforms or software environments. Like macOS, Windows , linux and android.

Event-Driven : An application that responds to input from the user (mouse movement, keystrokes, menu choices, etc.) or from messages from other applications. This is in contrast to a batch operation that continuously processes the next item from a group.

Real-time web Applications :  It is the technology that  enables users to receive information as soon as it is published by its authors, rather than requiring that they or their software check periodically for updates.

"Unified Programming Language"  : It is an attempt to create a programming language that combines the best features of all scripting and compiled languages - with none of their defects.
Q. Why use Node.js?
Node.js makes building scalable network programs easy. 
Some of its advantages include:
It is generally fast
It rarely blocks
It offers a unified programming language and data type
Everything is asynchronous 
It yields great concurrency


Q. What is the difference of JS from browser to JS on node.js
Ans. ( https://medium.com/swlh/what-is-node-js-and-how-does-it-differ-from-a-browser-ddebef00cbd9#:~:text=Unlike%20the%20browser%20where%20Javascript,can%20execute%20software%20and%20more )

REPL : A Read-Eval-Print Loop, or REPL, is a computer environment where user inputs are read and evaluated, and then the results are returned to the user.

Node.js uses Require to import modules whereas browser js uses Import
Node.js runs outside the client’s browser and Browser JS is run inside the browser
Node.js has full user level system access that means you can do anything you want, same as with C++, Java. Whereas javascript in the browser is sandboxed within the browser and you can’t have full user level system access like reading from file filesystem or writing to files in filesystem of user’s pc.
Node.js renamed Global object of js to Global because it doesn’t refer to the  window object.
Node is standalone capable of creating a full stack application with same features as any native application will have while we can’t do the same with browser’s javascript       

Q. Write three different ways to reverse a string in Javascript? a. using inbuilt method, b. iteratively, c. recursively
Ans. ( https://www.freecodecamp.org/news/how-to-reverse-a-string-in-javascript-in-3-different-ways-75e4763c68cb/ )

Q. Write a program to check two objects are equal ( deep equal )
Ans. https://www.samanthaming.com/tidbits/33-how-to-compare-2-objects/

Q. Explain some areas where you have seen currying being implemented in React / other libraries?
Ans. https://blog.logrocket.com/understanding-javascript-currying/#:~:text=Currying%20is%20a%20checking%20method,that%20can%20handle%20one%20responsibility

Q. IIFE ?
Ans. https://www.javascripttutorial.net/javascript-immediately-invoked-function-expression-iife/ 

Q. How does Node.js work?
A web server using Node.js typically has a workflow that is quite similar to the diagram illustrated below. Let’s explore this flow of operations in detail.

Node.js Architecture Workflow

Clients send requests to the web server to interact with the web application. Requests can be non-blocking or blocking:
Querying for data
Deleting data 
Updating the data
Node.js retrieves the incoming requests and adds those to the Event Queue
The requests are then passed one-by-one through the Event Loop. It checks if the requests are simple enough not to require any external resources
The Event Loop processes simple requests (non-blocking operations), such as I/O Polling, and returns the responses to the corresponding clients
A single thread from the Thread Pool is assigned to a single complex request. This thread is responsible for completing a particular blocking request by accessing external resources, such as computation, database, file system, etc.

Once the task is carried out completely, the response is sent to the Event Loop that sends that response back to the client.

Q. Does Node.js improve throughput? Why/How?
Ans. https://www.quora.com/Does-Node-js-improve-throughput-Why-How


Q. How do you explain throughput?
Ans. Throughput, in business, is the amount of a product or service that a company can produce and deliver to a client within a specified period of time. The term is often used in the context of a company's rate of production or the speed at which something is processed.

Q. How is Node js having high IO throughput?
Ans. ( https://javascript.plainenglish.io/understanding-nodejs-performance-dc9f2673455e )

Q. What are examples of CPU intensive tasks?
Ans. Sorting, search, graph traversal, matrix multiply are all CPU operations, a process is CPU-intensive or not it depends on how much and how frequent are their execution.

Q. How can you end up blocking your main thread in node.js?
Ans. ( https://www.geeksforgeeks.org/how-node-js-overcome-the-problem-of-blocking-of-i-o-operations/ )

Q. What is the event loop?
Ans. ( https://medium.com/@mmoshikoo/event-loop-in-nodejs-visualized-235867255e81#:~:text=The%20Event%20Loop%20sees%20that,(2)%20is%20being%20executed.&text=So%20the%20delay%20parameter%20in,which%20the%20function%20is%20executed )

Q. Phases of event loop?
Ans. ( https://medium.com/@kunaltandon.kt/process-nexttick-vs-setimmediate-vs-settimeout-explained-wrt-different-event-loop-phases-c0506b12921d#:~:text=The%20different%20phases%20of%20an,phase%20of%20the%20event%20loop )

Q. What is process.tick?
Ans. ( https://medium.com/@amanhimself/how-process-nexttick-works-in-node-js-cb327812e083 )

Q. When can process.tick starve your event loop?
Ans. ( https://medium.com/dkatalis/eventloop-in-nodejs-settimeout-setimmediate-vs-process-nexttick-37c852c67acb )

( https://www.youtube.com/watch?v=9RhOGoChGqo )

Q. What is the difference between setTimeout and setInterval?
Ans. The only difference is , setTimeout() triggers the expression only once while setInterval() keeps triggering expression regularly after the given interval of time.

( https://medium.com/@monica1109/scheduling-settimeout-and-setinterval-ca2ee50cd99f#:~:text=The%20only%20 difference%20is%20%2C,the%20given%20interval%20of%20time )

Q. How can you make a network request with http module from the backend?
Ans. ( https://medium.com/edureka/node-js-requests-6b94862307a2 )

Q. How can you create your own events?
Ans. ( https://www.freecodecamp.org/news/how-to-code-your-own-event-emitter-in-node-js-a-step-by-step-guide-e13b7e7908e1/ )

Q. What are clusters?
Ans. A sharded cluster in MongoDB is a collection of datasets distributed across many shards (servers) in order to achieve horizontal scalability and better performance in read and write operations.
( https://medium.com/@phoenixm103/creating-mongo-cluster-9578be417d16#:~:text=A%20MongoDB%20cluster%20is%20sharded,the%20nodes%20of%20the%20shard )

Q. How does your Node.js application handle scale? Elaborate
Ans. ( https://www.freecodecamp.org/news/scaling-node-js-applications-8492bd8afadc/ )

Q. What are CORS? How do you configure them? Why do you need them?
Ans. https://auth0.com/blog/cors-tutorial-a-guide-to-cross-origin-resource-sharing/ 

Q. What is rate limiting?
Ans. Rate limiting is a strategy for limiting network traffic. It puts a cap on how often someone can repeat an action within a certain timeframe – for instance, trying to log in to an account. Rate limiting can help stop certain kinds of malicious bot activity. It can also reduce strain on web servers. However, rate limiting is not a complete solution for managing bot activity.
https://www.cloudflare.com/en-in/learning/bots/what-is-rate-limiting/

Q. How does middleware work in express?
Ans. Middleware functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

https://medium.com/@adamzerner/middleware-in-express-60d75055ba8f 

Q. What is the difference between Encryption and Hashing?
Ans. Since encryption is two-way, the data can be decrypted so it is readable again. Hashing, on the other hand, is one-way, meaning the plaintext is scrambled into a unique digest, through the use of a salt, that cannot be decrypted.
( https://medium.com/swlh/the-difference-between-encoding-encryption-and-hashing-878c606a7aff#:~:text=%2D%20Encryption%20is%20a%20process%20to,into%20a%20fixed%2Dlength%20string )

Q. What is the difference between https and http?
Ans. Http vs https protocol
To summarize, HTTP delivers data and all files ( HTML, images, queries, etc) on the World Wide Web. HTTPS has been around since the very beginning of the internet. It has not received its fair share of attention until recently but that does not undermine the role it plays. As we learnt earlier, S stands for secure

( https://medium.com/@pallavimodi/http-https-what-is-the-difference-3a97fe2f7fd8#:~:text=To%20summarize%2C%20HTTP%20delivers%20data,on%20the%20World%20Wide%20Web.&text=HTTPS%20has%20been%20around%20since,earlier%2C%20S%20stands%20for%20secure )

Q. What is TLS?
Ans. https://medium.com/talpor/ssl-tls-authentication-explained-86f00064280#:~:text=TLS%20is%20a%20protocol%20for,the%20content%20of%20the%20messages 

Q.What is AES?
Ans. AES is a block cipher: it will receive 128 bits of text which will be transformed to obtain a different 128 bits of encrypted data. But 128 bits or 16 characters most probably won't be enough to fit all the data we wish to encrypt, so how does AES manage to encrypt whole documents filled up with text.
( https://medium.com/quick-code/understanding-the-advanced-encryption-standard-7d7884277e7#:~:text=AES%20is%20a%20block%20cipher,documents%20filled%20up%20with%20text%3F )

Q. What is JWT Token? Why do we need to use JWT? What are some pros and cons?
Ans. JWT : It is a definitely a clever way to securely get the identity of the client. In simple language there is a secret Key used to encrypt the JSON formatted Data which primarily includes the user-id. Now an encryption of data with the Key generates the token that is sent to the client and used in every request.
Ans. https://medium.com/@rahulgolwalkar/pros-and-cons-in-using-jwt-json-web-tokens-196ac6d41fb4#:~:text=JWT%20%3A%20It%20is%20a%20definitely,and%20used%20in%20every%20request

Q. What is salting? Where do we store salt?
Ans. https://medium.com/swlh/introduction-to-salted-hashed-passwords-d19bd6f92480#:~:text=A%20salt%20is%20a%20random,hashing%20function%20with%20a%20salt 

Q. What is V8?
Ans. https://medium.com/@duartekevin91/basics-of-understanding-chromes-v8-engine-c5c8ec61fa6b 

Q. What is difference between JS on the browser and node?
Ans. Unlike the browser where Javascript is sandboxed for your safety, node. js has full access to the system like any other native application. This means you can read and write directly to/from the file system, have unrestricted access to the network, can execute software and more.

https://medium.com/swlh/what-is-node-js-and-how-does-it-differ-from-a-browser-ddebef00cbd9#:~:text=Unlike%20the%20browser%20where%20Javascript,can%20execute%20software%20and%20more 

Q. What is the difference between Authorisation and Authentication?

Ans. Simply put, authentication is the process of verifying who someone is, whereas authorization is the process of verifying what specific applications, files, and data a user has access to. The situation is like that of an airline that needs to determine which people can come on board.

https://www.sailpoint.com/identity-library/difference-between-authentication-and-authorization/#:~:text=Simply%20put%2C%20authentication%20is%20the,people%20can%20come%20on%20board 

EVENT LOOPS IN NODE JS :
What is the Event Loop?

The event loop allows Node.js to perform non-blocking I/O operations by offloading operations to the system kernel whenever possible.

Since most modern kernels are multi-threaded, they can handle multiple operations executing in the background. When one of these operations completes, the kernel tells Node.js so that the appropriate callback may be added to the poll queue to eventually be executed.

When node.js starts it initialises the event loops and processes the given input script which may make async API calls, schedule timers or call process.nextTick( ) and begins processing the event loop.

Each phase of the event loop has a Queue of callbacks to be executed.
When the event loop enters any phase first it will  perform all the operations related to that phase then it will execute all the callbacks in that phase until the queue of callback is exhausted or maximum callback limit is reached then it will move to the next phase of the event loop.

What is kernel ? 
The kernel is a computer program at the core of a computer's operating system and generally has complete control over everything in the system. It is the portion of the operating system code that is always resident in memory, and facilitates interactions between hardware and software components.


Timers : This phase executes callbacks scheduled by setTimeout( ) and setInterval( ) 

Pending callbacks: This phase executes callbacks for some system operations like types of TCP error. For example, during a TCP connection if a socket receives an error then the system might want to report that error so for that time till the system reports the error it will queue this callback to execute in the pending callback phase. 

idle, prepare: only used internally. 

Poll : Retrieve new I/O events and executes I/O related callbacks except callbacks scheduled by timers, setImmediate( ) and closed callbacks.
 ​​The poll phase has two main functions:         
Calculating how long it should block and poll for I/O, then  Processing events in the poll queue.   
Check : setImmediate( ) callbacks are invoked here



When the event loop enters the poll phase and there are no timers scheduled, one of two things will happen:  
If the poll queue is not empty, the event loop will iterate through its queue of callbacks executing them synchronously until either the queue has been exhausted, or the system-dependent hard limit is reached.  
If the poll queue is empty, one of two more things will happen:  If scripts have been scheduled by setImmediate(), the event loop will end the poll phase and continue to the check phase to execute those scheduled scripts.  
If scripts have not been scheduled by setImmediate(), the event loop will wait for callbacks to be added to the queue, then execute them immediately.

Check : setImmediate() callbacks are invoked here.
This phase allows a person to execute callbacks immediately after the poll phase has completed. If the poll phase becomes idle and scripts have been queued with setImmediate(), the event loop may continue to the check phase rather than waiting.
Generally, as the code is executed, the event loop will eventually hit the poll phase where it will wait for an incoming connection, request, etc. However, if a callback has been scheduled with setImmediate() and the poll phase becomes idle, it will end and continue to the check phase rather than waiting for poll events.

NOTE : The main advantage to using setImmediate( ) over setTimeout( ) is setImmediate() will always be executed before any timers if scheduled within an I/O cycle, independently of how many timers are present.

process.nextTick( ) : 
After the current operation if completed, regardless of the current phase of the event loop, nextTickQueue will be processed by process.nextTick( ) and 
all the callbacks passed to the process.nextTick( ) will be resolved before the event loop continues. 
Which in some situations can starve the I/O by making a recursive process.nextTick( ) call, which prevents the event loop from reaching the poll phase.

process.nextTick() vs setImmediate() 
We have two calls that are similar as far as users are concerned, but their names are confusing.  
process.nextTick() fires immediately on the same phase 
setImmediate() fires on the following iteration or 'tick' of the event loop 



close callbacks : 
If a socket or handle is closed abruptly (e.g. socket.destroy()), the 'close' event will be emitted in this phase.

setImmediate() vs setTimeout() 
setImmediate() and setTimeout() are similar, but behave in different ways depending on when they are called. setImmediate() is designed to execute a script once the current poll phase completes. setTimeout() schedules a script to be run after a minimum threshold in ms has elapsed.
