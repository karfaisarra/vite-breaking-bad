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
            <h5>{{ character.name }}</h5>
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
    height: 100%;

    img {
        max-width: 100%;
        height: 350px;
        object-fit: cover;
    }

    h5 {
        color: $bb-light;
        padding-bottom: 0.75rem;
        padding-top: 0.5rem;
        text-transform: uppercase;
    }

    .category,
    .status {
        color: $bb-secondary;
    }
}
</style>