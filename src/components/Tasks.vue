<template>
    <div v-bind:key="task.id" v-for="task in tasks">
        <Task @del-task="$emit('del-task', task.id)" v-bind:task="task"/>
    </div>
</template>

<script>
import Task from './Task'
export default {
    name: 'Tasks',
    props: {
        tasks: Array,
    },
    components: {
        Task
    },
    emits: ['del-task'],
}

</script>