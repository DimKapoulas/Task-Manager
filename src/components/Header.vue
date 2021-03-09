<template>
    <header>
        <h1>{{ title }}</h1>
        <Button @click-btn="$emit('click-btn')" 
        :text="addTaskText ? 'Close' : 'Add Task'" 
        :color="addTaskText ? 'red' : 'green'"/>
    </header>
</template>


<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: String,
        addTaskText: Boolean
    },
    components: {
        Button
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: cente;
    margin-bottom: 20px;
}
</style>