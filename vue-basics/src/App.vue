<template>
  <h1>{{ title }}</h1>

  <h2>Add a new task</h2>

  <div>
   <input type="text"
     v-model="newTask"
     placeholder="Add a new task"
   >
  </div>

  <div v-if="newTask.length > 0">
   <h3>New task preview</h3>
   <p>{{ newTask }}</p>
 </div>

  <ul>
    <li v-for="task in tasks" :key="task.id">
      {{task.id}}. {{ task.name }}
        <div v-if="task.finished">
            <button>Delete task</button>
        </div>
         <div v-else-if="task.edit">
            <button>Edit task</button>
        </div>
        <div v-else>
            <p>No button</>
        </div>
    </li>
  </ul>

</template>

<script>
export default {
  data() {
    return {
      title: 'My To Do App',
      tasks: [
        { id: 1, name: 'Learn Vue JS', finished: false },
        { id: 2, name: 'Build a Vue application', finished: false },
        { id: 3, name: 'Write an article about Vue JS', finished: false }
      ]
    }
  }
}
</script>