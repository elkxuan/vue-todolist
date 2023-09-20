<template>
  <h1>To Do List</h1>
  <ul><todo-item v-for="x in items" :key="x" :item-name="x" style="background-color: darkgrey;"></todo-item><button @click="removeItem()">Remove</button></ul>
  <input v-model="newItem" @keydown.enter="addItem()">
  <button @click="addItem()">Add</button>
</template>

<script>
export default {
  data() {
    return {
      newItem: '',
      items: []
    };
  },
  methods: {
    addItem() {
      this.items.push(this.newItem);
      this.newItem = '';
    }
  }
}
</script>

