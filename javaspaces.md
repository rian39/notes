Freeman, Eric, Hupfer, Susanne, Arnold, Ken, JavaSpaces TM Principles, Patterns, and Practice, Addison-Wesley, 1999
The JavaTM programming language is arguably the most popular programming language in computing history-never before has a language so quicly achieved widespread use among computing professionals, students and hobbyists worldwide. 1 {#coding}


By early in the new millennium, a large class of computational devices – from desktop machines to small appliances and portable devices- will be network-enabled. This trend not only impacts the way we use computers, but also changes the way we create applications for them: distributed applications are becoming the natural way to build software. “Distributed computing” is all about designing and building applications as a set of processes that are distributed across a network of machines and work together as an ensemble to solve a common problem (2) {#ensemble} {#platform-definition}

JavaSpacesTM technology is a simple, expressive, and powerful tool that eases the burden of creating distributed applications. Processes are loosely coupled – communicating and synchronizing their activities using a persistent object store called a space, rather than through direct communication. (xv) {#ensemble} {#

Despite their benefits, distributed applications can be notoriously difficult to design, build and debug. The distributed environment introduces many complexities that aren't concerns when writing standalone applications. Perhaps the most obvious complexity is the variety of machine architectures and software platforms over which a distributed application must commonly execute. 3

The realities of a networked environment present many challenges beyond heterogeneity. By their very nature, distributed applications are built from multiple (potentially faulty) components that communicate over (potentially slow and unreliable) network links. These characteristics force us to address issues such as latency, synchronization, and partial failure that simply don't occur in standalone applications. 3

Note that the protocol is loosely coupled-HelloWorld writes an entry into the space without worrying about the specifics of which clients will access it, how many, from where, or when. Likewise, the HelloWorldClients don't care who generated the entry, where, or when; they simply use associative lookup to find it. They don't even care if the entry exists in the space or not, but are content to wait until it shows up.  15

The JavaSpacesTM Specification

Many distributed algorithms can be modeled as a flow of objects between participants. This is different from the traditional way of approaching distributed computing, which is to create method-invocation-style protocols between participants. In this architecture's "flow of objects" approach, protocos are based on the movement of objects into and out of implementations of JavaSpaces technology. 317

JavaSpaces services are tools for building distributed protocols. They are designed to work with applications that can model themselves as flows of objects through one or more servers. If your application can be modeled in this way, JavaSpaces will provide many benefits. 318
