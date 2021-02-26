<template>
    <div v-bind:key="task.id" v-for="task in tasks">
        <Task v-bind:task="task"/>
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
    }
}

</script>