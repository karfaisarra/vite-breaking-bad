<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header class="d-flex p-2">
        <img width="80" src="../assets/img/Breaking_Bad_logo.svg" alt="">
        <h1>Breaking Bad Api</h1>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

h1 {
    color: $bb-light;
}
</style>