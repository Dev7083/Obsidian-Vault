What data to be stored?

- Prisma -> helper -> object modeling  = ODM

- mongoose -> help in data modeling  = ODM

Install Mongoose:
```
npm i mongoose
```

Creating Model

```
import mongoose from 'mongoose';

const userSchema = new mongoose.Schema({});

export const User = mongoose.model('User', userSchema);
```

Defining Schema:
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

Timestamps:
- created At 
- updatedAt

Datapoint:



 