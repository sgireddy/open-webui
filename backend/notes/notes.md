# /api/v1/notes Endpoints

## List all notes
curl -X GET "http://localhost:52565/api/v1/notes/" -H "Authorization: Bearer <token>"

## Create a note
curl -X POST "http://localhost:52565/api/v1/notes/create" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"title": "Note Title", "content": "Note content", "user_id": "user01"}'

## Update note
curl -X POST "http://localhost:52565/api/v1/notes/{note_id}/update" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"title": "Updated Title"}'

## Delete note
curl -X DELETE "http://localhost:52565/api/v1/notes/{note_id}/delete" -H "Authorization: Bearer <token>"
