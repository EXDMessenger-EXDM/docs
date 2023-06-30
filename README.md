# docs
API docs for EXDM

# Me
```
GET http://127.0.0.1:3001/api/users/@me

Headers: {"Authorization": "token"}

{
  "avatar": "default.png",
  "banner": "default.png",
  "bot_variables": [],
  "connected_accounts": [],
  "discriminator": 3244,
  "email": "someemail@gmail.com",
  "flags": [],
  "guilds": [
    [
      "1",
      "DFC | Test",
      null,
      null,
      "6407958643072662934",
      "dfc",
      null,
      null,
      null,
      null
    ],
    null
  ],
  "id": 6407958643072662934,
  "status": 0,
  "username": "dragonfirex"
}

```

# AI
```
POST /api/ai/chatgpt-3.5 - Continue the message with chatgpt 3.5

JSON payload example: {"text": "Lorem ipsum"}
Response: {"text": "Lorem ipsum - стандартный набор слов-заполнителей, который используется в верстке и дизайне для наглядного представления внешнего вида готового продукта. Этот текст не несет в себе никакого осмысленного содержания и используется только для оценки компоновки и расположения элементов в макете."}
```

# Auth
```
POST /auth/login - Login to account
JSON payload example: {"email": "example@example.com", "password": "something123"}
Returns: {"token": "auth.token.for_exdm"}
Errors:
 - 404 - Account not found
 - 400 - Some fields is missing (Invalid JSON payload)
```
```
POST /auth/register - Register account
JSON payload example: {"username": "DragonFire", "password": "something123", "email": "example@example.com"}
Returns: {"token": "auth.token.for_exdm"}
Errors:
 - 400 - Some fields is missing (Invalid JSON payload)
```

# Guilds
```
GET /api/guilds/<path:guild_id> - Get guild info
```

# Commands
```
GET /api/commands - Get commands
JSON payload example: {"search": "ex"}

Returns [{"app_id": 1, "id": 1, "name": "example", "description": "Example command", "params": [{"id": 1, "type": "str", "name": "param1", "description": "Example description for param1"}]

⚠️ | Not in use at the moment, implemented for test purposes

Returns all slash commands (like Discord)
```

# Channels
```
GET /api/channels/<path:channel_id> - Get channel info
PATCH /api/channels/<path:channel_id> - Edit channel info

GET /api/channels/<path:channel_id>/messages - Get channel messages

GET /api/messages/<path:message_id> - Get message in channel
```
```
GET /api/channels/<path:channel_id>/messages - Get all messages in channel
Returns:
[{"author": 1, "channel_id": "global", "message": "First message!", "id": 1, "reactions": [], "attachments": []}, {"author": 1, "channel_id": "global", "message": "...and second!", "id": 2, "reactions": [], "attachments": []}]
```
```
POST /api/channels/<path:channel_id>/messages - Send message to channel
JSON payload example: {"content": "Hello everyone!"}
Returns: {'message': 'Write ok'} and 200 OK
```
