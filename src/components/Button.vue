<template>
    <button>
        {{ text }}
    </button>
</template>

<script>
    export default{
        name: 'Button',
        props: {
            text: {
                type: String,
                required: true
            }
        }
    }
</script>

<style scoped>
    button{
        width:100pt;
        height: 20pt;
        border: none;
        border-radius: 5pt;
        background-color: aqua;
    }
</style>