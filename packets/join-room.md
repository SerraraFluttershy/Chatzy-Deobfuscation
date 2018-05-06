# Join Room Packets

## Join 1

This is what is sent you click the 'join room'

- Destination: http://us{server}.chatzy.com/
- Type: GET
- Parameters:
  - jsonp:X7245: undefined
  - X5141: Identifier, if you're logged in
  - X5865: Room ID
  - X2940: Room Name, or ID
  - X7960: Chatzy Version
  - X5481: 1
  - X3190: "enter"
  - X6432: Room Nickname
  - X8049: Name Color, hex
  - X6577: Room Password/Admin Password
  - X5455: 2
  - X7245: "X6766"
  - X2457: Room Server
  - X7469: Current Timestamp, in milliseconds

## Join 2

You get this as the response of Join 1, and immediately send it back.
The room identifier will be used a lot, you can grab it here, it will also be part of the HTML response to this.

- Destination: http://us{server}.chatzy.com/{room_id}
- Type: POST
- Data:
  - X7960: Chatzy Version
  - X5481: 1
  - X1263: Room Identifier
  - X2798: ""
