<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{task.text}}
        <i class="fas fa-times"></i>
        </h3>
        <p>{{task.day}}</p>
    </div>
</template>

<script>
    export default {
        name: 'Task',
        props: {
            task: Object
        }
    }
</script>

<style scoped>
.task {
    background-color: #f4f4f4;
    margin: 5px;
    padding: 10px 20px;
    cursor: pointer;
}
.task.reminder {
    background-color: #cecece;
}
.task h3 {

}
</style>