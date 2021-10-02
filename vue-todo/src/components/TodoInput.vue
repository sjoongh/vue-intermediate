<template>
  <div>
    <input type="text" v-model="newTodoItem">
    <button v-on:click="addTodo">add</button>
  </div>
</template>

<script>
export default {
    data: function() {
        return  {
            newTodoItem: ""
        }
    },
    methods: {
        addTodo: function() {
            console.log(this.newTodoItem);
            // 저장하는 로직
            // localstoreage에 동일한 key, value값으로 저장
            localStorage.setItem(this.newTodoItem, this.newTodoItem);
            this.newTodoItem = '';
        }
    }
}
</script>

<style>

</style>