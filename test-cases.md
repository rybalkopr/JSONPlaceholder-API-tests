API Testing Project — JSONPlaceholder

Base URL: https://jsonplaceholder.typicode.com

Test Case 1: Get All Posts

Method: GET

Endpoint: /posts

Preconditions: Public API, no authentication required

Expected Result:

Status code: 200 OK

Response body is an array of 100 objects

Each object contains: userId, id, title, body

Test Case 2: Get Post by ID

Method: GET

Endpoint: /posts/1

Expected Result:

Status code: 200 OK

Response body is a single object

Object contains: userId, id, title, body

id = 1

Test Case 3: Create New Post

Method: POST

Endpoint: /posts

Headers: Content-Type: application/json

Request Body:

{
  "title": "Test Post",
  "body": "This is a test post body",
  "userId": 1
}

Expected Result:

Status code: 201 Created

Response body contains sent data + new id

Test Case 4: Update Post by ID

Method: PUT

Endpoint: /posts/1

Headers: Content-Type: application/json

Request Body:

{
  "id": 1,
  "title": "Updated Title",
  "body": "Updated body content",
  "userId": 1
}

Expected Result:

Status code: 200 OK

Response contains updated values

Test Case 5: Delete Post by ID

Method: DELETE

Endpoint: /posts/1

Expected Result:

Status code: 200 OK or 204 No Content

Empty or no response body

