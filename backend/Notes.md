# API Endpoint Summary with Example curl Statements

Assumptions:
- knowledge01, model01, team01 exist
- user01, user02 are part of team01
- model01 is based on knowledge01 and accessible to team01

---

## Example Endpoints (by Router)

### /api/v1/knowledge
- List all knowledge objects:
  curl -X GET "http://localhost:52565/api/v1/knowledge/" -H "Authorization: Bearer <token>"
- Get details for knowledge01:
  curl -X GET "http://localhost:52565/api/v1/knowledge/knowledge01" -H "Authorization: Bearer <token>"
- Create new knowledge:
  curl -X POST "http://localhost:52565/api/v1/knowledge/create" -H "Authorization: Bearer <token>" -d '{"name": "knowledge02", "team_id": "team01"}'
- Update knowledge01:
  curl -X POST "http://localhost:52565/api/v1/knowledge/knowledge01/update" -H "Authorization: Bearer <token>" -d '{"description": "Updated desc"}'
- Delete knowledge01:
  curl -X DELETE "http://localhost:52565/api/v1/knowledge/knowledge01/delete" -H "Authorization: Bearer <token>"

### /api/v1/models
- List all models:
  curl -X GET "http://localhost:52565/api/v1/models/" -H "Authorization: Bearer <token>"
- Get model01 details:
  curl -X GET "http://localhost:52565/api/v1/models/model?model_id=model01" -H "Authorization: Bearer <token>"
- Create new model:
  curl -X POST "http://localhost:52565/api/v1/models/create" -H "Authorization: Bearer <token>" -d '{"name": "model02", "knowledge_id": "knowledge01", "team_id": "team01"}'
- Update model01:
  curl -X POST "http://localhost:52565/api/v1/models/model/update" -H "Authorization: Bearer <token>" -d '{"model_id": "model01", "description": "Updated desc"}'
- Delete model01:
  curl -X DELETE "http://localhost:52565/api/v1/models/model/delete" -H "Authorization: Bearer <token>" -d '{"model_id": "model01"}'

### /api/v1/users
- List all users:
  curl -X GET "http://localhost:52565/api/v1/users/" -H "Authorization: Bearer <token>"
- Get user01 details:
  curl -X GET "http://localhost:52565/api/v1/users/user01" -H "Authorization: Bearer <token>"
- Update user01:
  curl -X POST "http://localhost:52565/api/v1/users/user01/update" -H "Authorization: Bearer <token>" -d '{"email": "user01@example.com"}'
- Delete user02:
  curl -X DELETE "http://localhost:52565/api/v1/users/user02" -H "Authorization: Bearer <token>"

### /api/v1/groups
- List all groups (teams):
  curl -X GET "http://localhost:52565/api/v1/groups/" -H "Authorization: Bearer <token>"
- Get team01 details:
  curl -X GET "http://localhost:52565/api/v1/groups/id/team01" -H "Authorization: Bearer <token>"
- Create new team:
  curl -X POST "http://localhost:52565/api/v1/groups/create" -H "Authorization: Bearer <token>" -d '{"name": "team02"}'
- Update team01:
  curl -X POST "http://localhost:52565/api/v1/groups/id/team01/update" -H "Authorization: Bearer <token>" -d '{"description": "Updated desc"}'
- Delete team01:
  curl -X DELETE "http://localhost:52565/api/v1/groups/id/team01/delete" -H "Authorization: Bearer <token>"

### /api/v1/notes
- List all notes for user01:
  curl -X GET "http://localhost:52565/api/v1/notes/" -H "Authorization: Bearer <token>"
- Create a note:
  curl -X POST "http://localhost:52565/api/v1/notes/create" -H "Authorization: Bearer <token>" -d '{"title": "Note Title", "content": "Note content", "user_id": "user01"}'
- Update note:
  curl -X POST "http://localhost:52565/api/v1/notes/<note_id>/update" -H "Authorization: Bearer <token>" -d '{"title": "Updated Title"}'
- Delete note:
  curl -X DELETE "http://localhost:52565/api/v1/notes/<note_id>/delete" -H "Authorization: Bearer <token>"

---

## Auth Example
- Sign in:
  curl -X POST "http://localhost:52565/api/v1/auths/signin" -d '{"username": "user01", "password": "password"}'
- Get current user:
  curl -X GET "http://localhost:52565/api/v1/auths/" -H "Authorization: Bearer <token>"

---

## More endpoints available for chats, files, folders, pipelines, etc. See routers for full details.
