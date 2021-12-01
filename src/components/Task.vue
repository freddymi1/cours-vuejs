<template>
    
    <div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'tasks']">
        <div>
            <h3>#{{task.id}}</h3>
            <h3>{{task.text}}</h3>
            <h3>{{task.day}}</h3>
            <h3>{{task.reminder}}</h3>
        </div>
        <div class="btnAction">
            <button @click="$emit('delete-task', task.id)" class="btn btn-danger btn-sm"> <i class="fas fa-trash"></i></button>
            <button class="btn btn-success btn-sm"> <i class="fas fa-eye"></i></button>
        </div>
    </div>
    
</template>

<script>
    export default {
        name: "Task",
        props: {
            task: Object
        }
        // ,
        // methods: {
        //     onDelete(id){
        //         // console.log(id)
        //         this.$emit('delete-task', id)
        //     }
        // }
    }
</script>

<style scoped>
.tasks{
    position: relative;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    background: rgb(224, 224, 224);
    margin-top: 1rem;
    border-radius: 0 15px 15px 0;
    cursor: pointer;
}

.reminder{
    border-left: 4px solid green;
}
.tasks h3{
    font-size: 1.2rem;
}
.btnAction{
    position: absolute;
    right: 1rem;
    display: flex;

}
</style>