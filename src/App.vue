<script>
export default {
  data() {
    return {
      todoList: ["Première tache","Premier commit","Initiliasation du projet"]
    }
  },
  methods:{
    addTodo(){},
    editTodo(){},
    deleteTodo(){}
  },
  mounted(){
    console.log("Welcome dans la todo list Vue JS 3")
  }
}
</script>

<template>
  <div>
    <h2>Todo List</h2>
  </div>
  <div>
    <input name="tache" type="text">
    <button @click="addTodo()">Ajouter</button>
  </div>
    <ul v-if="todoList.length>0">
      <li v-for="todo in todoList">
        {{ todo }}
        <button @click="editTodo()">Modifier</button>
        <button @click="deleteTodo()">Supprimer</button>
      </li>
    </ul>
    <h4 v-else>Pas de tache(s)</h4>
</template>

<style scoped>
</style>
