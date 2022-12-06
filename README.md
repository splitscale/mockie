# Usage Guideline

### Javascript interface

- POST method payload
  **Object you need to send**

Body

```
  interface User {
    id: number;
    username: string;
    password: string;
  }
```

- GET method payload
  **Object you will get**

Body

```
  interface UserDisplayable {
    id: number;
    username: string;
  }
```

### Endpoints

- `/api/user/create`

  - Request body: `User`
  - Response body: `UserDisplayable`

- `/api/user/get`

Correct username is: `stevenBallaret`

  - Request body: none
  - Response body: `UserDisplayable`

- `/api/user/update`

  - Request body: `User`
  - Response body on error: `username or password is empty`: `status code: 400`

- `/api/user/delete`

  - Request body: `User`
  - Response body on error: `username or password is empty`: `status code: 400`