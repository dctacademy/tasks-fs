# Backend API for tasks app 

## Installation 
* goto https://github.com/dctacademy/tasks-fs
* run the command `git clone https://github.com/dctacademy/tasks-fs.git`
* go inside the tasks-fs folder 
* install the packages with `npm install` 
* run the backend server with `node app.js` 


## API Documentation
### Tasks Resource 

| # | action | method | url | request | response | authentication |
| ----- |-----|-------|--------|---------|------| ------|
| 1. | lists all tasks | GET | /api/tasks | - | empty array or array of objects <br/> | no auth | 
| 2. | create a task | POST | /api/tasks  | <ul><li>name*</li> <li>mobile*</li> <li> email </li></ul> | <ul> <li>_id</li> <li> name </li> <li>mobile</li><li>email</li> <li>user</li><li>createdAt</li> <li>updatedAt</li> </ul>| `{ Authorization : 'Bearer token'}` |
| 3. | get a task | GET | /api/tasks/:id  | - | <ul> <li>_id</li> <li> name </li> <li>mobile</li><li>email</li> <li>user</li><li>createdAt</li> <li>updatedAt</li> </ul> | `{ Authorization : 'Bearer token'}` |
| 4. | update a task | PUT | /api/tasks/:id  | <ul><li>name*</li> <li>mobile*</li> <li> email </li></ul> | <ul> <li>_id</li> <li> name </li> <li>mobile</li><li>email</li> <li>user</li><li>createdAt</li> <li>updatedAt</li> </ul> | `{ Authorization : 'Bearer token'}` |
| 5. | delete a task | DELETE | /api/tasks/:id  | - | <ul> <li>_id</li> <li> name </li> <li>mobile</li><li>email</li> <li>user</li><li>createdAt</li> <li>updatedAt</li> </ul> | `{ Authorization : 'Bearer token'}` |
