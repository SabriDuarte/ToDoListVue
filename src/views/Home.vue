<template>
    <div class="datos">
        <input type="text" v-model="task" placeholder="Ingrese una tarea">
        <button @click="add">Agregar Tarea</button>
        <pending-tasks :listTask='listTask'></pending-tasks>
    </div>
</template>

<script>
    import PendingTasks from '../components/PendingTasks';
    export default {
        name:'Home',
        components: {
            PendingTasks,
        },
        data(){
            return{
                task:'',
                listTask:[],
            }
        },
        methods: {
            add(){
                let tarea = this.task;
                if(tarea.length >0){
                    this.listTask.push(tarea)
                    console.log(this.listTask)
                    this.task = ''
                }
            }
        },
    }

</script>