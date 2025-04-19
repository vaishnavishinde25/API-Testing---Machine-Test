# FFC Postman API Test

##  Environment Setup
- Create a new environment in Postman:
  - 'base_url`: `https://testffc.nimapinfotech.com`
  - 'username': `siddiqshaikh1@nimapinfotech.com'
  - 'password`: `admin@123'

##  API Collection Structure
### 1. Login - Valid
- Method: `POST'
- URL: `{{base_url}}/api/login'
- Body:
```json
{
"email": "{{username}}",
  "password": "{{password}}"
}
```
-  Stores `auth_token` in environment.

### 2. Login - Invalid
- Incorrect login to verify validation.

### 3. Add Customer
- Method: `POST'
- URL: `{{base_url}}/api/customers/add'
- Header: `Authorization: Bearer {{auth_token}}'
- Body:
```json
{
  "name": "API Test User",
  "email": "apitestuser@example.com",
  "phone": "9876543210"
}
```



