# /api/v1/auths Endpoints

## Get current session user
curl -X GET "http://localhost:52565/api/v1/auths/" -H "Authorization: Bearer <token>"

## Sign in
curl -X POST "http://localhost:52565/api/v1/auths/signin" -H "Content-Type: application/json" -d '{"email": "user01@example.com", "password": "password"}'

## Sign up
curl -X POST "http://localhost:52565/api/v1/auths/signup" -H "Content-Type: application/json" -d '{"name": "user01", "email": "user01@example.com", "password": "password"}'

## Update profile
curl -X POST "http://localhost:52565/api/v1/auths/update/profile" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"profile_image_url": "/user.png", "name": "user01"}'

## Update password
curl -X POST "http://localhost:52565/api/v1/auths/update/password" -H "Authorization: Bearer <token>" -H "Content-Type: application/json" -d '{"password": "oldpass", "new_password": "newpass"}'

## LDAP login
curl -X POST "http://localhost:52565/api/v1/auths/ldap" -H "Content-Type: application/json" -d '{"user": "user01", "password": "password"}'

## Generate API key
curl -X POST "http://localhost:52565/api/v1/auths/api_key" -H "Authorization: Bearer <token>"

## Delete API key
curl -X DELETE "http://localhost:52565/api/v1/auths/api_key" -H "Authorization: Bearer <token>"

## Get API key
curl -X GET "http://localhost:52565/api/v1/auths/api_key" -H "Authorization: Bearer <token>"
