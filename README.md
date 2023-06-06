# Movie Booking Service - Resful Api

## Environment
- Node V18.16.0
- NestJS

## API Document
### Front End
#### User Login
1. Sign up: `Post` -> `/api/user/signup`
   ```json
   # Post body
   {
    "email": "string",
    "password": "string",
    "checkPassword": "string"
   }
   # Response - success
   {
    "status": "success",
    "data": {
        "email": "string",
        "jwt": "string"
    }
   }
   ```
2. Login: `Post` -> `/api/user/login`
   ```json
   # Post body
   {
    "email": "string",
    "password": "string",
   }
   # Response - success
   {
    "status": "success",
    "data": {
        "email": "string",
        "jwt": "string"
    }
   }
   ```
3. Forget Password: `Post` -> `/api/user/password/forget`
   ```json
   # Post body
   {
    "email": "string"
   }
   # Response - success
   {
    "status": "success",
    "data": {
        "email": "string"
    }
   }
   ```
#### Home
4. home info: `Get` -> `/api/home`
   - Current Movies
   - ComingSoon Movies
   - Activities
   ```json
   # Response - success
   ```
#### Movies
5. Movie List: `Get`  -> `/api/movies`
   ```json
   # Response - success
   ```
#### Activities
6. Activities List: `Get` -> `/api/activities`
   ```json
   # Response - success
   ```
#### Theaters
7. Theater List: `Get` -> `/api/theaters`
   ```json
   # Response - success
   ```

#### User
8. User info: `Get` -> `/api/user/infos`
   - Personal info
   - consumption record
   - Point
   ```json
   # Response - success
   ```
9.  Save edit user info: `Patch` -> `/api/user/infos`
    ```json
    # Response - success
    ```
10. Save Edit password: `Patch` -> `/api/user/password`
    ```json
    # Response - success
    ```

#### Ticket
11.  Movie info: `Get` -> `/api/ticket/movie/:movieId`
    - movie introduction
    - movie sessions
    ```json
    # Response - success
    ```
12.  Session info: `Get` -> `/api/ticket/session/:sessionId`
    - movie info
    - sessions time in every area
    ```json
    # Response - success
    ```
13.  Seats info in specific session: `Get` -> `/api/ticket/session/:sessionId/seats`
    ```json
    # Response - success
    ```
14.  Check Seats avaliable `Post` -> `/api/ticket/session/:sessionId/seats`
    ```json
    # Response - success
    ```
15. Save Counsumption record `Post` -> `/api/user/consumption`
    ```json
    # Response - success
    ```

- All response fail
```json
# Response - Fail
{
    status: "fail",
    message: "error message"
}
```


### Management System
#### admin
1. login
2. users list
3. add user
4. save edit user
#### theater CRUD
5. theaters list
6. add theater
7. edit theater
8. close theater

#### activities CRUD
9. activities list
10. add activity
11. edit activity
12. remove activity

#### movie CRUD
13. movies list
14. add movie
15. edit movie - 要考慮臨時下檔影響場次的問題

#### room CRUD
16. romms list in theater
17. add room
18. edit room
19. close room

#### seats Sample CRUD
20. seats list
21. add seats
22. edit seats
23. close seats

#### ticket Sample CRUD
24. tickets list
25. add tickets
26. edit ticket
27. close ticket

#### session CRUD
25. add session
26. edit session


- All response fail
```json
# Response - Fail
{
    status: "fail",
    message: "error message"
}
```