<template>
    <div :key="item.id" v-for="item in tasks">
        <Task @toggle-reminder="$emit('toggle-reminder', item.id)" @delete-task="$emit('delete-task', item.id)" :task="item"/>
    </div>
</template>

<script>
import Task from "./Task";

export default {
    name: 'Tasks',
    props: {
        tasks: Array
    },
    components: {
        Task
    },
    emits: ['delete-task', 'toggle-reminder']
}
</script>