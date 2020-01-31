
# Server streams

When a client is subscribed to a channel, sometimes
it doesn't make sense to receive all the messages from that channel.

For example, if we have 3000 chat rooms, subscribing to `ChatChannel`
and receiving messages from all chat rooms is not too useful.

But if we somehow specify one chat room to get messages from
then that's more useful.

The server is the one that determines which messages
will a subscription get, and it can accept certain parameters
from the client to determine that.

So let's say we want to subscribe to just the room of id `351`, we do it like so:

```javascript
consumer.subscriptions.create({ channel: "ChatChannel", room: 351 })
```

Then in the body of `subscribed` method of that channel we have
to determine that this new subscriber will receive messages only from room `351`.

```ruby
# app/channels/chat_channel.rb
class ChatChannel < ApplicationCable::Channel
  def subscribed
    stream_from "chat_#{params[:room]}"
  end
end
```

This way, when someone sends a message to "chat_351", our beforementioned user will
receive it.
