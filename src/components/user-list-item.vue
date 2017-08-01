<template>
    <div class="user" :class="isActive">
        {{user.name}} <button v-on:click="sayName">Speak!</button>
    </div>
</template>

<script>
    export default {
        props: ['user', 'selectedUserIndex', 'index'],
        computed: {
        isActive() {
            return {
                active: this.selectedUserIndex === this.index
            }
        }
        },
        methods: {
            sayName() {
                this.$emit('sayName')
            }
        }
    }
</script>

<style>
    .active {
        color: red;
    }
</style>
