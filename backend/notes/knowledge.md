# /api/v1/knowledge Endpoints

## List all knowledge objects
curl -X GET "http://localhost:52565/api/v1/knowledge/" -H "Authorization: Bearer <token>"

## Get knowledge by ID
curl -X GET "http://localhost:52565/api/v1/knowledge/{knowledge_id}" -H "Authorization: Bearer <token>"

## Create new knowledge
curl -X POST "http://localhost:52565/api/v1/knowledge/create" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"name": "Knowledge Name", "team_id": "team01"}'

## Update knowledge
curl -X POST "http://localhost:52565/api/v1/knowledge/{knowledge_id}/update" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"description": "Updated desc"}'

## Delete knowledge
curl -X DELETE "http://localhost:52565/api/v1/knowledge/{knowledge_id}/delete" -H "Authorization: Bearer <token>"
