
## What?

> "A system in which the failure of a computer you didn't even know existed can render your own computer unusable" - Leslie Lamport 

- Multiple computers/machines typically communicating over a network
- Can involve all elements of usual [[execution]], but since a network and different environments are getting involved - things get tricky.

## Why?

Some applications are inherently distributed. Example, sending message from your phone to your friend's phone - no two ways about it.

But other reasons why you may choose to have distributed systems could be:

- Better reliability: Even if one node fails, system as a whole keeps functioning
- Better performance: Get data from nearby node, rather than one halfway around the world
- To solve bigger problems: Huge amounts of data - can't fit on one machine
- Different applications/services talking to each other: Your app might need to talk to other applications or services over network. 

## Why NOT?

- Communications can fail -- and we might not even know it.
- Malicious players
- Processes themselves may crash - other systems might not be aware of it.
- All these failures may happen nondeterministically.

## Why study?

The main challenge of having distributed systems is to keep them **fault tolerant** -- whole system should work despite failures of some parts.

**TIP** If it can be done on one computer -> keep it that way 

## References

- [Distributed Systems Lecture Series - Dr. Martin Kleppmann](https://www.youtube.com/watch?v=UEAMfLPZZhE&list=PLeKd45zvjcDFUEv_ohr_HdUFe97RItdiB)