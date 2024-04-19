---
id: 44htsikkj5eek54erdet52y
title: Application with No Constraints
desc: ''
updated: 1708447229538
created: 1708447133119
---

#interview-question

[Link to stackOverflow question](https://stackoverflow.com/questions/64003764/design-an-application-with-no-constraints?noredirect=1#comment113242537_64003764)

How will you design an app which -

- Performs a number of tasks
- the tasks can be anything (any operation or program or literally just anything)
- there can be any number of tasks
- those tasks can have any number of inputs
- the task to be done may be sent as a payload
- the inputs may be sent as payload
- there can be any number of clients.
- the client can send any kind of request (GET, PUT, POST etc.)

List the classes and interfaces you'll create and describe the entire flow of the application. Everything should be "loosely-coupled".

## StackOverflow conversation since the post got deleted

> This sounds almost like a project that you want someone to hire you to do. Mind you, the first part of the solution would not even be classes, it will be infrastructure, like what is the platform you're targeting, languages etc. This is quite a loaded thing, and if you were asked this in an interview I guarantee you the interviewer did not want you to list classes or interfaces but wanted to see your experience designing distributed systems and knowledge of basic things like producer-consumer, distributed queues, concurrent execution etc,. – 
zaitsman
 Sep 23, 2020 at 0:15

> I actually talked about the infrastructure to him. But he specifically asked to forget all that and tell him all the classes and interfaces I'll use for this kind of system. – 
Chinmay Singh
 Sep 24, 2020 at 3:49   

> Well, that just shows that the interviewer might need to work on asking, as the question is heaps open ended. Nevertheless, you need an input endpoint, a status check endpoint, a results grab endpoint (regardless of HTTP/TCP/other RPC protocol), a repository to fetch results (persisted somehow), a queue producer, a queue consumer, a task processor, and a repository to store results, most of these would be abstracted via CQRS or Service-Layer architecture and will thus have both an interface and a concrete implementation. – 
zaitsman
 Sep 24, 2020 at 3:54