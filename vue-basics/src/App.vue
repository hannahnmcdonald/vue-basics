<template>
  <h1>{{ title }}</h1>

  <ul>
    <li v-for="task in tasks" :key="task.id">
      {{task.id}}. {{ task.name }}
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