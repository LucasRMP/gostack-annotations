# SEQUELIZE AND ORM

## WHAT IT IS SEQUELIZE?

- Sequelize is an **ORM** (Object Relational Mapper) built for **Node.js** that works with SQL databases **ONLY**

## WHAT IS ORM?

- ORM is an **abstraction** of databases, usually to the **MVC** (Model, View, Controller) structure
- **Tables** becomes **Models**
- Working with the tables will translate to the **Controllers**

## DATA MANIPULATION

- We will **almost never** use SQL, just **JS** code

---

```sql
  INSERT INTO users (username, email)
    VALUES ( "LucasRMP", "lucas.rmp@test.com" )
```

**TURNS INTO**

```js
User.create({
  username: "LucasRMP",
  email: "lucas.rmp@test.com"
});
```

---

```sql
  SELECT *
  FROM users
  WHERE email = "lucas.rmp@test.com"
  LIMIT 1
```

**TURNS INTO**

```js
User.findOne({
  where: {
    email: "lucas.rmp@test.com"
  }
});
```

## MIGRATIONS

- Is an version control for our database
- Kind of a log of all the **changes** that has been made and how to undo them
- **Each file is a different migration** and they are ordered by date, from oldest to newest
- Each migration has a `up()` and a `down()`
  - The `up()` function specifies how to **DO** the modification
  - The `down()` function specifies how to **UNDO** the modification
- **IMPORTANT**: Once the migration is somewhere out of our machine, we can **NEVER** change it, otherwise we may experience **inconsistence** between our dev team or in production
- Each migration should affect **only one table**, for bigger changes you can always create multiple migrations

```js
  module.exports = {
  up: (queryInterface, Sequelize) => {
    return queryInterface.createTable('Person', {
      name: Sequelize.DataTypes.STRING,
      isBetaMember: {
        type: Sequelize.DataTypes.BOOLEAN,
        defaultValue: false,
        allowNull: false
      }
    });
  },
  down: (queryInterface, Sequelize) => {
    return queryInterface.dropTable('Person');
  }
```

## SEEDS

- Tools for **populating the database** with **fake** data for development pruposes
- Much used for **tests enviroment**
- Are **never** used in production
- In case you want to include **default rows** in a table for production, do a **migration**
