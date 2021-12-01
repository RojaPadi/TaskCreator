# Task Creator

### Requirement
##### Task

 - Contains 2 attributes (description and status).
 - Status have 2 status (complete or incomplete).
 - Task can have multiple sub tasks.
 - Sub Task can never be dependent on parent task.
 - A task is complete only when all sub tasks are complete. 

### API Endpoints

##### Task
	
```
 Task Response
 {
	 id	 
	 desciption
	 status	
	 createdAt
	 updatedAt
	 SubTasks 
 }
```

 - Create
 ```
 ### Request ###
 type: POST
 url : api_url/tasks
 body: {
	 description: <descrition>
 }
 
 Response
 Task Response
 ```
 
 - Update Task
```
Request
type: patch
url : api_url/tasks/:id
body: {
	description
}

Response
Task Response
```

 - Delete Task
```
Request 
type: delete
url : api_url/id

Response
Code: 204
```

 - Add Sub Task
 ```
 Request
 type: post
 url : api_url/tasks/:id/subTask
 body:{
	 id: <SubTaskId>
 }

Response
TaskResponse
 ```

- Delete Sub Task
```
Request
type: delete
url : api_url/tasks/:id/subTask
body:{
	id: <SubTaskId>
}

Response
code: 204
```

 - Update Status ( Change Task Status to Complete)
 ```
 Request
 type: patch
 url : api_url/tasks/:id/status
 
 Response
 TaskResponse
 ```
 
 - Update Status ( Change Task Status to In Complete)
 ```
 Request
 type: delete
 url : api_url/tasks/:id/status
 
 Response
 TaskResponse
 ```


