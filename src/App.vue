<template>
  <div className="header-background">
    <Navbar  title="Kolot'sart"/>
    <div class="content">
      <Home/>

      <Tasks @toggle-reminder="toggleReminder" @delete-task="deleteTask" :tasks="tasks" />
    </div>
  </div>
</template>

<script>
/**
 * Import all components
 */
import Navbar from './components/Layout/Navbar'
import Home from './components/Home'
import Tasks from './components/Tasks'
export default {
  name: 'App',
  components: {
    Home,
    Navbar,
    Tasks
  },
  data(){
    return{
      tasks: []
    }
  },

  methods: {
    deleteTask(id){
      if(confirm("Are you sur to want to delete this task?")){
        this.tasks = this.tasks.filter((task)=> task.id !== id)
      }
    },

    toggleReminder(id){
      this.tasks = this.tasks.map((task)=> task.id === id ? {...task, reminder: !task.reminder} : task)
    }
  },
  created(){
    this.tasks = [
      {
        id: 1,
        text: "Doctors appointements",
        day: 'March 1st at 2:30pm',
        reminder: true
      },
      {
        id: 2,
        text: "Shopping",
        day: 'April 12nd at 9:30am',
        reminder: false
      },
      {
        id: 3,
        text: "Sport",
        day: 'Mai 3rd at 1:30pm',
        reminder: true
      }
    ]
  }
}
</script>

<style>

  /* .header-background {
    position: static;
    display: block;
    overflow: visible;
    top: 0;
    height: 100vh;
    width: 100%;
    background-image: -webkit-gradient(
      linear,
      left top,
      left bottom,
      from(rgba(50, 58, 69, 0.9))
    ) !important; */
    /* background: linear-gradient(
        -90deg,
        rgba(50, 58, 69, 0.55),
        rgba(50, 58, 69, 0.74)
      ),
      url("./assets/images/bg.png") !important; */
    /* flex-direction: column !important;
    background-position: 0px 0px, 100% 50% !important;
    background-size: auto, cover !important;
    white-space: normal !important;
    object-fit: fill !important; */
    /* -o-object-fit: fill !important; */
  /* } */
  .content{
    padding: 0 4rem;
    margin-top: 3rem;
  }
  button{
      padding: 0.5rem 1rem;
      background: rgb(41, 39, 39);
      color: #fff;
      font-weight: 600;
      border: none;
      cursor: pointer;
      transition: all .3s ease;
  }
  button:hover{
      background: rgb(29, 28, 28);
  }
</style>
