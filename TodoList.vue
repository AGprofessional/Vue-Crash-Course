<template>
    <h1>TodoList</h1>
</template>

{https://www.youtube.com/watch?v=PWgCqzmi0TQ&list=PLRAV69dS1uWTpHQgiV4rZFlnuS8XDl71A&index=4
}

<script>
export default{
data(){
    return {
        todos: [
            {todoString: "todo1", completed: true},
             {todoString: "todo2", completed: true},
              {todoString: "todo3", completed: true},
               {todoString: "todo4", completed: true},
            
        ]
    }
},
methods: {
    addTodo(newTodo){
        this.todos.push({
            todoString: newTodo, completed: false
        })
        },
    toggleTodo(todo){
        todo.completed = !todo.completed
    },
    editTodo(todo, newTodoString){
        todo.todoString =newTodoString;

    },
    deleteTodo(deleteTodo){
        this.todos = this.todos.filter(todo => todo !== deleteTodo)
    }
}
}
</script>

<style>

</style>