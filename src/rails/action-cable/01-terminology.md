
# Terminology

Here's a list of details:

* An action cable server can handle multiple **connections**
* There is **one connection per websocket connection**
* A single user may have **multiple websockets** connected to the application
* The client of a websocket connection is called the **consumer**
* Each **channel** is conceptually similar to a **controller**
* Each consumer can subscribe to **multiple channels**
* A consumer subscribed to a channel is called a **subscriber** of it
* A connection between a subscriber and a channel is called a **subscription**
* A consumer can be subscribed to the same channel multiple times
* Every channel can **stream** zero or more **broadcastings**
* A broadcasting is a pubsub link where anything transmitted by the broadcaster is sent directly to the channel subscribers who are streaming that named **broadcasting**

## PubSub

PubSub is a message queing paradigm where senders send data to an abstract class of recipients,
without specifying individual recipients.
