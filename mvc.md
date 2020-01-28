# MVC ARCHITECTURE

## MODEL

- It holds the **database abstraction**, its role is to do every data manipulation that a database would do
- **NOT** responsable for our application's **business rules**

## CONTROLLER

- Is the **entry point** of our application, a route is usually associated with one controller's method
- **Responsable** for most of our application's **business rules**
- When **scaling** an application, it is a good practice to **isolate** the **business rules**

### Structure

- Is usually a `class`
- Should have only **5 methods**
- Always will return an **JSON**
- A controller method should **NEVER** call a method of **another controller** or from **itself**
- We should create a new Controller every time we have a new entity on our application

```js
class UserController {
  index() {} // List all the users

  show() {} // Show only one user

  store() {} // Create a new user

  update() {} // Update some data of a user

  delete() {} // Delete a user
}
```

## VIEW

- Is the **return** for the **client**
- In applications that **doesn't use the restful** architecture this layer can be a **HTML** that is returned when a route is called
- In our case this layer will be mostly **JSON** that will be returned to the **front end**, who will be responsible for **manipulating the data**
