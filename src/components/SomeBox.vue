<template>
    <label>
        The box
        <input type="text" v-model="boxVal" @keyup="logBox">
    </label>
</template>

<script>
    export default {
        name: "SomeBox",
        methods: {
            logBox () {
                alert(this.boxVal)
            }
        },
        data() {
            return {
                boxVal: ''
            }
        }
    }
</script>

<style scoped>

</style>