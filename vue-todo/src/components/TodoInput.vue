<template>
    <div class="inputBox shadow">
        <input type="text" v-model="newTodoItem">
        <button v-on:click="addTodo">ADD</button>
        <span class="addContainer"></span>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            newTodoItem: ""
        }
    },
    methods: {
        addTodo: function() {
            // eslint-disable-next-line
            // console.log(this.newTodoItem);
            // 저장하는 로직
            localStorage.setItem(this.newTodoItem, this.newTodoItem);
            this.clearInput();
        },
        clearInput: function() {
            this.newTodoItem = '';
        }
    }
}
</script>

<style scopped>
input :focus {
    outline: none;
}
.inputBox {
    background: 
}
</style>
