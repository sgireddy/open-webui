# /api/v1/chats Endpoints

## List all chats
curl -X GET "http://localhost:52565/api/v1/chats/" -H "Authorization: Bearer <token>"

## Create new chat
curl -X POST "http://localhost:52565/api/v1/chats/new" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"title": "Chat Title", "model_id": "model01"}'

## Import chat
curl -X POST "http://localhost:52565/api/v1/chats/import" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"chat_data": {}}'

## Search chats
curl -X GET "http://localhost:52565/api/v1/chats/search?query=example" -H "Authorization: Bearer <token>"

## Archive all chats
curl -X POST "http://localhost:52565/api/v1/chats/archive/all" -H "Authorization: Bearer <token>"

## Pin chat
curl -X POST "http://localhost:52565/api/v1/chats/{id}/pin" -H "Authorization: Bearer <token>"

## Delete chat
curl -X DELETE "http://localhost:52565/api/v1/chats/{id}" -H "Authorization: Bearer <token>"
