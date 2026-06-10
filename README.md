### Backend 4 Dummies

Backend 4 Dummies is a series of articles, breaking down fundamental concepts in Backend Development in the simplest terms possible. It both a tool for my own understanding, which I reference when I'm at my most confused, but also my attempt to teach those who are new to these concepts. 

With Software Concepts, I generally find high-strung theory clearifying **AFTER** I understsand its application. Meaning that in these articles, I'll take an "example first, theory later" approach. 

The first question, I'd like to begin with is: 

**How does the internet actually work?** As in, what actually is going on, when I type in a website url, and I'm magically transported to a new website. I think even the most 'shallow' explanation of the client-server model, will pay dividends in you understanding of the internet, as such lets begin! 

### The Client Server Model 


I want you to imagine a web, and on these web there are nodes, and connections between them. *The Internet*  is these entire web, and **computers** are the nodes.

When you try and connect to another website, your simply trying to connect to another server, and retrieve some information. 

All of this communication happens through HTTP requests: 

The Client is the computer / server making the initial request. It's you googling "free flights" at 12am. 

The Server is the one **recieving** the request. 

*To be clear, servers can/do act as clients, and clients can act as servers as well. The distinction betweeen the two typically is what first triggers in the data transaction between the two devices* 


