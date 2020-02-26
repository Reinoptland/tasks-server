# How to use this example

1. clone
2. install deps

```shell
npm install
```

3. run

```
npm start
```

4. Or run with nodemon

```
npm run dev
```

## HTTPIE commands to test

Create a user

```shell
http POST :4000/users email=rein@rein.io
```

Get a user with id `1`

```shell
http GET :4000/users/1
```

Update a user with id `1` change the email to rein@rein.ai

```shell
http PUT :4000/users/1 email=rein@rein.ai
```

Get all the tasks for a user with id `1`

```
http GET :4000/users/1/tasks
```

Create a task for a user with id `1`, the description of the task is: Learn sequelize

```
http POST :4000/users/1/tasks description="Learn sequelize"
```

Get the task with id `2` belonging to the user with id `1`

```
http GET :4000/users/1/tasks/2
```

Update the description of task with id `2` belonging to the user with id `1` to: Be awesome

```
http PUT :4000/users/1/tasks/2 description="Be awesome"
```

Delete a task with id `2` belonging to the user with id `1`

```
http DELETE :4000/users/1/tasks/2
```

Delete all tasks belongin to the user with id `1`

```
http DELETE :4000/users/1/tasks
```
