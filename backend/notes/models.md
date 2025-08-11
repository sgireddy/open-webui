# /api/v1/models Endpoints

## List all models
curl -X GET "http://localhost:52565/api/v1/models/" -H "Authorization: Bearer <token>"

## Get model by ID
curl -X GET "http://localhost:52565/api/v1/models/model?model_id={model_id}" -H "Authorization: Bearer <token>"

## Create new model
curl -X POST "http://localhost:52565/api/v1/models/create" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"name": "Model Name", "knowledge_id": "knowledge01", "team_id": "team01"}'

## Update model
curl -X POST "http://localhost:52565/api/v1/models/model/update" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"model_id": "model01", "description": "Updated desc"}'

## Delete model
curl -X DELETE "http://localhost:52565/api/v1/models/model/delete" -H "Authorization: Bearer <token>" -d '{"model_id": "model01"}'
