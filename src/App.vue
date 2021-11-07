<template>
<div class="container">
      <Header title="Task Tracker!!" />
      <Tasks :tasks="tasks" />
</div>
</template>

<script>
import Header from './components/Header'
import Tasks from './components/Tasks'

export default {
  name: 'App',
  components: {
    Header,
    Tasks
  },
  data() {
    return {
      tasks: []
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: '밥먹기',
        day: '2021.10.2',
        reminder: true
      },
      {
        id: 2,
        text: '아침 운동하기',
        day: '2021.11.10',
        reminder: true
      },
      {
        id: 3,
        text: '인강보기',
        day: '2021.11.22',
        reminder: false
      },
      {
        id: 4,
        text: '책읽고 독후감',
        day: '2021.11.28',
        reminder: false
      },
    ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
  background-color: #333;
  color:#fff;
  padding: 10px 20px;
  border-radius: 4px;
  border: none;
  font-size: 20px;
}
</style>
