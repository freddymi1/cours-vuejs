<template>
    <div>
        <Button text="Add task" color="#50b28d"/>
        <!-- <Button text="Update task" color="#25bcad"/>
        <Button text="Delete task" color="#c22020"/> -->
    </div>
</template>

<script>
import Button from './Button.vue'
export default {
    name: 'Home',
    // props: ['title']
    props: {
        
        // title: {
        //     type: String,
        //     default: 'Hello word'
        // }
    },
    components: {
        Button
    }
}
</script>
<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>