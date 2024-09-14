
> [!NOTE] Pre requisite
>  - A programming Lang {Java, Js, PHP, golang, C++}
>  -  A Database {MOngoDB, MySQL, Postgress, Sqlite}

---
A  JS based Backend
1. Data
2. File
3. Third Party API

A  JS Runtime: 
- ==Node JS / Deno / Bun==
---

**File/Folder Structure**

- Src
	-  index
	- app
	- constants
- DB
- Models
- Controllers
- Routes
- Middlewares
- Utils
- Package.json
- .env
- Readme/git/lint/prettier
---
![[./images/one.png]]

---

**Initialization:-**
```
npm init
```
Adding Express JS:-
```
npm install express
```
Hello World in Express:-
```javascript
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})
```

Run:-
```
npm run <script-name>
```
For Hot reloading:-
	Install Nodemon

Set up .env for Universal compatibility:-

```
npm i dotenv
```

Dotenv Usage:-
```
require('dotenv').config()
console.log(process.env)
```
Using ES6:-
```
//Using ES6
import 'dotenv/config'
console.log(process.env.variable_name)
```

Common JS vs Module JS:-

- Common JS -> synchronous -- require
```
const express = require('express')
```


- Module JS -> asynchronous -- import
```
import express from 'express';
```

- type in "package.json" defines whether to assemble in common js or module.
```
 "type":"module",
```
