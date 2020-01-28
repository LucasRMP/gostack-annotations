# REST / RESTFUL API

## HOW DOES IT WORK ?

- Has a **request / response** flow
  - **Request** made from a **client** _(Browser usually)_
  - **Response** given by the **Server**
  - The **client** gets the response and processes the data

## HTTP METHODS

- **GET**: Used when you want to retrieve some information from the server
- **POST**: Used when you want to create some information on the server
- **PUT**: Used when you want to alter / modify some information on the server
- **DELETE**: Used when you want to delete an information on the server

## BENEFITS

- **Multiple clients** _(front-ends)_ can use the same **backend** _(scalability)_
- Unified communication protocol: Same structure for web, mobile or public API

## JSON

**GLOBAL FRONT <--> BACK END COMMUNICATION PROTOCOL**

```json
{
  "User": {
    "name": "Lucas Pessone",
    "email": "lucas.rmp@teste.com",
    "techs": ["REACT", "REACT_NATIVE", "NODEJS"],
    "company": {
      "name": "Rocketseat",
      "url": "https://rocketseat.com.br"
    }
  }
}
```

## REQUEST PAYLOAD

<code> 
  <span style="color:yellow">GET</span> http://api.com/<span style="color:#7159c1">company</span>/<span style="color:#70A861">1a5wq7f5</span>/<span style="color:#7159c1">users</span><span style="color:#C62373 ">?page=2</span>
</code>

- ![#7159c1](https://placehold.it/15/7159c1/000000?text=+) Route
- ![#70A861](https://placehold.it/15/70A861/000000?text=+) Route Params
- ![#C62373](https://placehold.it/15/C62373/000000?text=+) Query Params

<code> 
  <span style="color:yellow">POST</span> http://api.com/<span style="color:#7159c1">company</span>/<span style="color:#70A861">1a5wq7f5</span>/<span style="color:#7159c1">users</span>
</code>

```json
  "User": {
    "name": "Lucas Pessone",
    "email": "lucas.rmp@teste.com",
    "techs": ["REACT", "REACT_NATIVE", "NODEJS"]
  }
```

- The json part is called **BODY**

## HTTP CODES

- <span style="color:cyan">1xx</span> - Informational
- <span style="color:rgb(50,255,50)">2xx</span> - Success
  - <span style="color:rgb(50,255,50)">200</span> - SUCCESS
  - <span style="color:rgb(50,255,50)">201</span> - CREATED
- <span style="color:rgb(200,0,255)">3xx</span> - Redirection
  - <span style="color:rgb(200,0,255)">301</span> - MOVED PREMANENTLY
- <span style="color:yellow">4xx</span> - Client **error**
  - <span style="color:yellow">400</span> - BAD REQUEST
  - <span style="color:yellow">401</span> - UNAUTHORIZED
  - <span style="color:yellow">404</span> - NOT FOUND
- <span style="color:red">5xx</span> - Server **error**
  - <span style="color:red">500</span> - INTERNAL SERVER ERROR
