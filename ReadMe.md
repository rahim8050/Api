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
- Add Users [Post] 
```
bash
http://localhost:8000/api/users/
```
- Profile [Get]
```
bash
http://localhost:8000/api/users/profile/
{
  "_id": "507f1f77bcf86cd799439011",
  "name": "John Doe",
  "email": "john@example.com",
  "createdAt": "2025-05-16T05:20:00.000Z"
}
```
- Update Profile [Patch]
```
bash 
http://localhost:8000/api/users/profile/
```
- Change Password [Post]
```
bash 
http://localhost:8000/api/users/change_password/
```
## Example usage












