# Project: 0x03. User authentication service

## Resources

#### Read or watch:

* [Flask documentation]
* [Requests module]
* [HTTP status codes]

# 0x03. User authentication service

## About
A session based user authentication API

## Files
- [app.py](app.py): API entry point 
- [auth.py](auth.py): authentication model
- [db.py](db.py): database model
- [user.py](user.py): user model
- [main.py](user.py): end-to-end integration tests
 
 ## Setup
 ```
 $ pip3 install -r requirements.txt
 ```
## Run
```
$ flask run
```

## Routes
- `GET /`: returns logout message when user is logged out
- `GET /profile` returns email of logged in user
- `POST /users`: creates new user (Form data: `email`, `password`)
- `POST /sessions`: logs in existing user(Form data: `email`, `password`)
- `POST /reset_password`: returns password reset token (Form data: `email`)
- `PUT /reset_password`: updates existing user's password (Form data: `email`, `new_password`, `reset_token`)
- `DELETE /sessions`: logs out user

## Tasks

| Task | File |
| ---- | ---- |
| 0. User model | [user.py](./user.py) |
| 1. create user | [db.py](./db.py) |
| 2. Find user | [db.py](./db.py) |
| 3. update user | [db.py](./db.py) |
| 4. Hash password | [auth.py](./auth.py) |
| 5. Register user | [auth.py](./auth.py) |
| 6. Basic Flask app | [app.py](./app.py) |
| 7. Register user | [app.py](./app.py) |
| 8. Credentials validation | [auth.py](./auth.py) |
| 9. Generate UUIDs | [auth.py](./auth.py) |
| 10. Get session ID | [auth.py](./auth.py) |
| 11. Log in | [app.py](./app.py) |
| 12. Find user by session ID | [auth.py](./auth.py) |
| 13. Destroy session | [auth.py](./auth.py) |
| 14. Log out | [app.py](./app.py) |
| 15. User profile | [app.py](./app.py) |
| 16. Generate reset password token | [auth.py](./auth.py) |
| 17. Get reset password token | [app.py](./app.py) |
| 18. Update password | [auth.py](./auth.py) |
| 19. Update password end-point | [app.py](./app.py) |
| 20. End-to-end integration test | [main.py](./main.py) |
