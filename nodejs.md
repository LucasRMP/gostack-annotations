# NODE.JS

## WHAT IS NODE.JS?

- Node is a **runtime enviroment** _(not a framework)_ to run javascript on the backend using the V8 engine with a C++ encapsulation
- We do **NOT** deal with final user's events
- The only way to listen to user events is through the application **routes**

---

## WHAT IS NPM / YARN?

- They are both **packager managers** that are used to install **third party libs**
- They make it possible for us to share **our libs** with the community
- Yarn is **faster** and has a lot of **features** than npm has:
  - Working with multiple projects with the same dependencies in the same folder

---

## NODE STRUCTURE

- Event Loop:

  - Event base architecture
  - Has a **call stack**
  - Has a **single threaded** event loop
  - C++ lib called **libuv** is used behind the scenes and uses multithreading processing

- Non-blocking I/O (**Socket\.IO**)

---

## FRAMEWORKS

### EXPRESS

- No opinion - **NOT** a fixed structure
- **Micro-Framework**

### AdonisJS

- Has opinion / a fixed structure
- Great for productivity
