# docs
API docs for EXDM

# AI
```
POST /api/ai/chatgpt-3.5 - Continue the message with chatgpt 3.5

JSON payload example: {"text": "Lorem ipsum"}
```

# Channels
```
GET /api/channels/<path:guild_id>/<path:channel_id> - Get channel info
PATCH /api/channels/<path:guild_id>/<path:channel_id> - Edit channel info

GET /api/channels/<path:guild_id>/<path:channel_id>/messages - Get channel messages
POST /api/channels/<path:guild_id>/<path:channel_id>/messages - Send message to channel

GET /api/channels/<path:guild_id>/<path:channel_id>/<path:message_id> - Get message in channel
```
