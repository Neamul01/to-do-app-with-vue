<template>
  <div>
    <div class="font-bold uppercase text-2xl">To do list</div>
    <div class="my-2">
      <input type="text" name="Add" v-model="value" id="" class="border-2 p-1 pl-2" />
      <button class="border-2 p-1 px-3" @click="addToDo()">Add</button>
      <ToDoList :todo='todo' @removelist="emptyList" />
    </div>
  </div>
</template>

<script lang="ts">
import ToDoList from './components/ToDoList.vue'

export default {
  components: {
    ToDoList
  },
  data() {
    return {
      todo: ['Write some code', 'learn new tech'],
      value: ''
    }
  },
  methods: {
    addToDo() {
      this.todo.push(this.value);
      this.value = ''
    },
    emptyList() {
      this.todo = []
      console.log('please remove the list')
    }
  }
}
</script>