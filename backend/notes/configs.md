# /api/v1/configs Endpoints

## Import config
curl -X POST "http://localhost:52565/api/v1/configs/import" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"config": {}}'

## Export config
curl -X GET "http://localhost:52565/api/v1/configs/export" -H "Authorization: Bearer <token>"

## Get connections config
curl -X GET "http://localhost:52565/api/v1/configs/connections" -H "Authorization: Bearer <token>"

## Set connections config
curl -X POST "http://localhost:52565/api/v1/configs/connections" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"connections": {}}'
