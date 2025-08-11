# /api/v1/users Endpoints

## List all users
curl -X GET "http://localhost:52565/api/v1/users/" -H "Authorization: Bearer <token>"

## Get user by ID
curl -X GET "http://localhost:52565/api/v1/users/{user_id}" -H "Authorization: Bearer <token>"

## Update user
curl -X POST "http://localhost:52565/api/v1/users/{user_id}/update" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"email": "user01@example.com"}'

## Delete user
curl -X DELETE "http://localhost:52565/api/v1/users/{user_id}" -H "Authorization: Bearer <token>"
