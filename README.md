# TaskCreator
tree tasks project

tasks :
    ->Task has multiple sub tasks
    ->Children of the task must not be its parent.
    ->Task is done when all the subTasks has done.

EndPoints : 
    Create Task:
    ->Request : 
      TYPE : POST 
      URL  : /tasks
      BODY : {
          description
      }
    ->Response : 
      {
          id : '',
          description : '',
          status : '',
          createdAt: '',
          updatedAt  : ''
      }
    Update Task:
    ->Request :
    TYPE : PATCH
    URL  : /tasks/:id
      BODY : {
          description:'',
          status : ''
      }
    ->Response :  
        {
          id : '',
          description : '',
          status : '',
          createdAt: '',
          updatedAt  : ''  
        }

    Delete Task:
    ->Request :
    TYPE : DELETE
    URL  : /tasks/:id

  add SubTask:
  ->Request :
   TYPE : POST
   URL : /tasks/:id/subTask
   BODY : {
     subtaskId : ''
   }
  -> Response
  {
    subtask/task
  }

  delete SubTask:
  ->Request :
   TYPE : DELETE
   URL : /tasks/:id/subTask/:id

   Update Sub Task:
    ->Request :
    TYPE : PATCH
    URL  : /tasks/:id/subTask/:id
      BODY : {
          
      }
    ->Response :  {
      subTask
    }
        




