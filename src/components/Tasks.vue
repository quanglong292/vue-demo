<template>
    <div :key="item.id" v-for="item in tasks">
        <Task :task="item"/>
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
    }
}
</script>