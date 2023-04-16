# docs
API docs for EXDM

# AI
```
POST /api/ai/chatgpt-3.5 - Continue the message with chatgpt 3.5

JSON payload example: {"text": "Lorem ipsum"}
Response: {"text": "Lorem ipsum - стандартный набор слов-заполнителей, который используется в верстке и дизайне для наглядного представления внешнего вида готового продукта. Этот текст не несет в себе никакого осмысленного содержания и используется только для оценки компоновки и расположения элементов в макете."}
```

# Channels
```
GET /api/channels/<path:channel_id> - Get channel info
PATCH /api/channels/<path:channel_id> - Edit channel info

GET /api/channels/<path:channel_id>/messages - Get channel messages
POST /api/channels/<path:channel_id>/messages - Send message to channel

GET /api/messages/<path:message_id> - Get message in channel
```
