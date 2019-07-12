# API Challenge

## Users

### Create

Creates user.

`POST http://challenge.payparty.com.br/users`

```
body: {
  name: Fulano da Silva,
  email: f.silva@domain.com,
  password: 1234
}
```

### Auth

Authenticates user.

`POST http://challenge.payparty.com.br/users/auth`

```
body: {
  email: f.silva@domain.com,
  password: 1234
}
```

## To-Do

### Create

Creates to-do item.

`POST http://challenge.payparty.com.br/users/:user/todo`

```
params: {
  user: ObjectId
},
body: {
  value: String
}
```

### Update

Modifies to-do item.

`PUT http://challenge.payparty.com.br/users/:user/todo/:todo`

```
params: {
  user: ObjectId,
  todo: ObjectId
},
body: {
  value: String
}
```

### Delete

Deletes to-do item.

`DELETE http://challenge.payparty.com.br/users/:user/todo/:todo`

```
params: {
  user: ObjectId,
  todo: ObjectId
}
```

### Get by user

Gets all to-do items created by user.

`GET http://challenge.payparty.com.br/users/:user/todo`

```
params: {
  user: ObjectId
}
```