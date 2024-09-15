
Mongoose is an Object Data Modeling (ODM) library for MongoDB. MongoDB is a NoSQL database and Mongoose is used to interact with MongoDB by providing a schema-based solution. The Mongoose acts as the abstraction layer over the MongoDB database. It is generally preferred over using normal MongoDB because it simplifies the process of sending complex queries.

Usage:
Mongoose is used in Node application to interact with MongoDB without write complex queries. It acts as an Object Data Modeling (ODM) used to define schema model and provides easy communication between application and database. It provides many features like schema validation, middleware support, and easy query building It manages relationships between data, and is used to translate between objects in code and the representation of those objects in MongoDB.

Advantages:
- Schema Definition:
- Data Validation:
- Middleware Support:
- Query Building:
- Modeling Relationships and Population:



Installation:
```
npm i mongoose
```

Model Creation:
```
import mongoose from 'mongoose';

const userSchema = new mongoose.Schema({});

export const User = mongoose.model('User', userSchema);
```

Schema Definition:
```
const userSchema = new mongoose.Schema(
  {
    username: {
      type: String,
      required: true,
      unique: true,
      lowercase: true,
    },

    email: {
      type: String,
      required: true,
      unique: true,
      lowercase: true,
    },

    password: {
      type: String,
      required: [true, 'password is required'],
    },
  },
  { timestamps: true }
);
```


Image:(Buffer Files)
- stored in AWS Bucket / Cloudinary
 - public URL address is passed as a string format in DB


### TODO Data Modeling


## E-Commerce data Modeling



## Hospital Data Modeling



