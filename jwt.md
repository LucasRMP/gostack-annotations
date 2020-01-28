# JWT

- JSON Web Token
- It is a way to control session

  <span style="color:green">POST</span> http://api.com/<span style="color:pink">sessions</span>

  ```json
  {
    "email": "some@email.com",
    "password": "123456"
  }
  ```

- The routes goes to the database, does all necessary verifications and then returns for us a **JWT**
- We generate it from a library and use to authenticate in the different routes of our application

---

## STRUCTURE

<pre><code><span style="color:#7159c1">eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9</span>.<span style="color:#70A861">eyJpc3MiOiJ0b3B0YWwuY29tIiwiZXhwIjoxNDI2NDIwODAwLCJodHRwOi8vdG9wdGFsLmNvbS9qd3RfY2xhaW1zL2lzX2FkbWluIjp0cnVlLCJjb21wYW55IjoiVG9wdGFsIiwiYXdlc29tZSI6dHJ1ZX0</span>.<span style="color:#C62373">yRQYnWzskCZUxPwaQupWkiUzKELZ49eM7oWxAQK_ZXw</span></code></pre>

- ![#7159c1](https://placehold.it/15/7159c1/000000?text=+) Headers: Type and algorithm used to generate it
- ![#70A861](https://placehold.it/15/70A861/000000?text=+) Payload: Aditional data (user_id)
- ![#C62373](https://placehold.it/15/C62373/000000?text=+) Signature
