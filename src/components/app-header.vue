<template>
    <div class="header">
        <h1>{{title}}</h1>
    </div>
</template>

<script>
    export default {
      data() {
        return {
          title: 'the header!!!'
        };
      }
    }
</script>

<style scoped>
    .header {
        color: blue;
    }
</style>