<template>
  <div>
    <div class="pending">
      <h3>Tareas Pendientes!!</h3>
      <ul v-for= "(task,index) in listTask" :key="index">
        <li>{{task}}
          <input type="checkbox" :name="task">
          </li>
      </ul>

    </div>
    <div class="done">
      <h3>Tareas Hechas</h3>
      <ul v-for="(task,index) in completeTask" :key="index">
        <li>{{task}}
          <input type="checkbox" v-model="checked" @click="stateTasks">
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
export default {
  name: 'PendingTasks',
  props: {
    listTask: String
  },
  data(){
    return{
      checked: false,
      completeTask: [],
      state:''
    }
  },
  methods: {
    stateTasks (){
      let state = this.checked;
      if(state != false){
        this.completeTask.push(state.task)
      }
      console.log(state)
    }
  },
}
</script>
<style scoped>
  h3{
    text-align: center;
  }
  input{
    justify-content: center;
  }
</style>

