# /api/v1/channels Endpoints

## List all channels
curl -X GET "http://localhost:52565/api/v1/channels/" -H "Authorization: Bearer <token>"

## Create new channel
curl -X POST "http://localhost:52565/api/v1/channels/create" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"name": "Channel Name"}'

## Get channel by ID
curl -X GET "http://localhost:52565/api/v1/channels/{id}" -H "Authorization: Bearer <token>"

## Post message to channel
curl -X POST "http://localhost:52565/api/v1/channels/{id}/messages/post" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"content": "Hello world"}'

## Add reaction to message
curl -X POST "http://localhost:52565/api/v1/channels/{id}/messages/{message_id}/reactions/add" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"reaction": "👍"}'

## Delete message
curl -X DELETE "http://localhost:52565/api/v1/channels/{id}/messages/{message_id}/delete" -H "Authorization: Bearer <token>"
