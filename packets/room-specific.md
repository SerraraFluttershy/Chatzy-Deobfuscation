# Room Specific Packets

This set includes how to post messages, check for new messages, check current visitor list, etc.

## Post Message
Will send a message to the room. Will also return any new messages that have been sent since the Current Offset,
and the new Current Offset and Last Received Timestamp

- Destination: http://us{server}.chatzy.com/
- Type: POST
- Data:
  - X7960: Chatzy Version
  - X7245: "X2928"
  - X1263: Room Identifier
  - X7162: Current Offset
  - X9102: Last Received Timestamp
  - X7974: Message Text
  - X6746: 1
- Headers:
  - Host: us{server}.chatzy.com
  - Refferer: http://us{server}.chatzy.com/{room_id}
  
## Get Messages
Will return any new messages that have been sent since the Current Offset, and will return
new Current Offset and Last Received Timestamp.

- Destination: http://us{server}.chatzy.com/
- Type: GET
- Params:
  - "check:{room_id}"
  - Key (Bunch of uppercase letters, don't fully understand it yet)
  - Last Received Timestamp
  - Current Offset
  - Random Decimal