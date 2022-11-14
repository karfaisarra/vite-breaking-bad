<script>
export default {
    name: 'CharacterItem',
    props: {
        character: Object
    }
}
</script>
<template>
    <div class="col">
        <div class="character">
            <img :src="character.img" :alt="character.name">
            <h3>{{ character.name }}</h3>
            <div class="category">{{ character.category }}</div>
            <div class="status">{{ character.status }}</div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

.character {
    padding: 1rem;
    background-color: $bb-dark;
    text-align: center;
    height: 460px;

    img {
        max-width: 100%;

    }

    h3 {
        color: $bb-light;
    }

    .category,
    .status {
        color: $bb-secondary;
    }
}
</style>