
# Client subscription

A consumer can subscribe to a given channel.

```javascript
// app/javascript/channels/chat_channel.js
import consumer from "./consumer"
 
consumer.subscriptions.create({ channel: "ChatChannel" })
 
// app/javascript/channels/appearance_channel.js
import consumer from "./consumer"
 
consumer.subscriptions.create({ channel: "AppearanceChannel" })
```
