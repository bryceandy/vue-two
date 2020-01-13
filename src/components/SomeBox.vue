<template>
    <div class="some-box">
        <label>
            The box
            <input type="text" v-model="boxVal">
        </label>
        <button @click="logBox">Submit</button>
        <ul class="places">
            <li v-bind:key="name.length" v-for="name in names" v-text="name"/>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "SomeBox",
        methods: {
            logBox () {
                this.names.push(this.boxVal);
                this.boxVal = ''
            }
        },
        data() {
            return {
                boxVal: '',
                names: ['Arusha', 'Manyaraa', 'Ruuvuma', 'Twara']
            }
        }
    }
</script>

<style scoped>
    * {
        font-size: large
    }
    button {
        margin: 1em;
        padding: .5em
    }
</style>