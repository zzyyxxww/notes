---
wip: true
---

# Server side connections

There is one for every websocket accepted by the server.
This object is the **parent of all channel subscriptions** created from then on.

It shouldn't do any application logic, just authenticating and authorizing.

The client of this is called a **consumer**.

This is an instance of `ApplicationCable::Connection`.

```ruby
# app/channels/application_cable/connection.rb
module ApplicationCable
  class Connection < ActionCable::Connection::Base
    identified_by :current_user
 
    def connect
      self.current_user = find_verified_user
    end
 
    private
      def find_verified_user
        if verified_user = User.find_by(id: cookies.encrypted[:user_id])
          verified_user
        else
          reject_unauthorized_connection
        end
      end
  end
end
```

`identified_by` identifies a connection by some value.  
You can access a connection later with that identifier.

In the example, we are identifying connections by users.  
If no user is found, connections are rejected.

Cookies are sent through websockets, so you can access that in your
connections to authenticate users.

*Note: it is expected that the authentication is
also handled somewhere else in the app.*
