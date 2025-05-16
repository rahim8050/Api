# User Management API
A simple RESTful API for creating and managing user data with full CRUD (Create, Read, Update, Delete) functionality.

## Table of Contents
### Features 
### Technologies 
### Installation 
### Configuration 
## Testing
### API Endpoints 
### Example Usage
### Contributing
### License 
## Features
- Create new user accounts.
- Retrieve user details (single user or all users).
- Update existing user information.
- Delete user accounts.
- Input validation and error handling.

## Technologies
- Language: [ Python]
- Framework: [Django]
- Database: [SQlite]
- Other Tools: [Postman,Simple Jwt]

## Configuration
- Clone the repository:
```bash 
    git clone https://github.com/rahim8050/API
```
- Install dependencies:
``` bash 
pip install djangorestframework-simplejwt
```

## Set up the database:
- Ensure [your database] is running.
- Run migrations 
-Start the server
```bash
python manage.py runserver
```
### Testing
- Use Postman or any API client to test the endpoints.




### API endpoints
- login user [Post]
```
bash
http://127.0.0.1:8000/login
```
### Response
```
{
  "status": "success",
  "tokens": {
    "refresh": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTc0NzQ3NjMwMSwiaWF0IjoxNzQ3Mzg5OTAxLCJqdGkiOiIwNmEwOGI3ODQ5M2I0ZTU2YTZmZTE5MWY2N2ZmNzgwZCIsInVzZXJfaWQiOjV9.I4g9o3Ndv_viQPZcVTil2HHycVhxzlurMIOqoVMwFBM",
    "access": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNzUyNTczOTAxLCJpYXQiOjE3NDczODk5MDEsImp0aSI6IjQzODRhMDdmMzFmMzQ1NTlhMzk4ZmVmZGZmMzIwZjliIiwidXNlcl9pZCI6NX0.AI0S9Rh2WfuIcGmlpMoFKaLtAHcd3TO1HUWIHsC79B8"
  },
  "user": {
    "id": 5,
    "email": "test@t.com"
  }
}
```
- Add Users [Post] 
```
bash
http://localhost:8000/api/users/
```
### Response
``` json
{
  "email": "test@t.com",
  "first_name": "Test",
  "last_name": "Test_L"
}
```
- Profile [Get]
```
bash
http://localhost:8000/api/users/profile/

```
### Response
``` json
{
  "id": 5,
  "email": "test@t.com",
  "first_name": "Test",
  "last_name": "TTT",
  "is_staff": false,
  "is_active": true
}
```

- Update Profile [Patch]
```
bash 
http://localhost:8000/api/users/profile/
```
### Response
``` json
{
  "user": {
    "id": 5,
    "email": "test@t.com",
    "first_name": "Test",
    "last_name": "TTTy",
    "is_staff": false,
    "is_active": true
  },
  "message": "Profile updated successfully"
}
```
- Change Password [Post]
```
bash 
http://localhost:8000/api/users/change_password/
```
### Response
```json
{
  "status": "password changed"
}
```
- Delete User [Delete]
``` bash
http://127.0.0.1:8000/api/users/delete_me/

```
### Response
```json

```