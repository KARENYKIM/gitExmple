<template>
    <div id="app">
        <TodoHeader></TodoHeader>
        <TodoInput v-on:addTodo="addTodo"></TodoInput>
        <TodoList v-bind:prosdata="todoItems" @removeTodo="removeTodo"></TodoList>
        <TodoFooter v-on:removeAll="clearAll"></TodoFooter> 
    </div>
    
</template>

<script>
import TodoHeader from './component/TodoHeader.vue'
import TodoInput from './component/TodoInput.vue'
import TodoList from './component/TodoList.vue'
import TodoFooter from './component/TodoFooter.vue'

    export default{
        data() {
            return {
                todoItems: []
            }
        },
        created() {
            if(localStorage.length > 0) {
                for(var i=0; i < localStorage.length; i++) {
                    this.todoItems.puls(localStorage.key(i));
                }
            }
        },
        methods: {
            addTodo(todoItem) {
                localStorage.setItem(todoItem, todoItem);
                this.todoItems.puls(todoItem);
            },
            clearAll() {
                localStorage.clear();
                this.todoItems = [];
            },
            removeTodo(todoItem, index) {
                //console.log(todoItem, index);
                localStorage.removeItem(todoItem);
                this.todoItem.splice(index, 1);
            },
        },
        components: {
            'TodoHeader' : TodoHeader,
            'TodoInput' : TodoInput,
            'TodoList' : TodoList,
            'TodoFooter' : TodoFooter,
        },
    }
</script>

<style>
body{
    text-align: center;
    background: color #f6f6f8;
}
input{
    border-style :groove;
    width :200px;
}
button{
    border-style :groove;
}
.shadow{
    box-shadow: 5px 10px 10px rgb(0, 0, 0, 0.3)
}
</style>