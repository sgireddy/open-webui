# /api/v1/groups Endpoints

## List all groups
curl -X GET "http://localhost:52565/api/v1/groups/" -H "Authorization: Bearer <token>"

## Get group by ID
curl -X GET "http://localhost:52565/api/v1/groups/id/{group_id}" -H "Authorization: Bearer <token>"

## Create new group
curl -X POST "http://localhost:52565/api/v1/groups/create" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"name": "Group Name"}'

## Update group
curl -X POST "http://localhost:52565/api/v1/groups/id/{group_id}/update" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"description": "Updated desc"}'

## Delete group
curl -X DELETE "http://localhost:52565/api/v1/groups/id/{group_id}/delete" -H "Authorization: Bearer <token>"
