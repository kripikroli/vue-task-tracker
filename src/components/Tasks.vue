<template>
    <div v-bind:key="task.id" v-for="task in tasks">
        <Task @toggle-reminder="$emit('toggle-reminder', task.id)" @del-task="$emit('del-task', task.id)" v-bind:task="task"/>
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
    emits: ['del-task', 'toggle-reminder'],
}

</script>