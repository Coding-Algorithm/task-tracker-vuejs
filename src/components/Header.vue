<template>
    <header>
        <h1>{{ title }}</h1>
        <Button :showAddTask="showAddTask" @btn-click="$emit('toggle-add-task')"
            :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'red' : 'green'" />
    </header>
</template>

<script>
import Button from './Button.vue'


export default {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean
    },
    components: {
        Button
    },
    methods: {
        onClick() {
            this.$emit('toggle-add-task')
        }
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>


