
# Client consumers

From the client side, we connect by creating a consumer.

```javascript
// consumer.js
import { createConsumer } from "@rails/actioncable"
 
export default createConsumer()
```

This will prepare a websocket connection to `/cable` by default.
Keep in mind that the actual connection is attempted when any subscription is attempted.

The consumer can also take an argument that specifies the URL to connect to.

```javascript
// consumer.js
// Specify a different URL to connect to
export default createConsumer('https://ws.example.com/cable')
```
