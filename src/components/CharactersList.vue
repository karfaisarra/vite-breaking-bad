<script>
import CharacterItem from './CharacterItem.vue'
import { store } from '../store.js'
export default {
    name: 'CharactersList',
    components: {
        CharacterItem,
    },
    props: {
        characters: Array
    },
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <section class="characters">
        <div class="container p-3">
            <div class="found  p-2">
                <p v-if="store.characters !== null">Found {{ store.characters.length }} characters</p>
            </div>
            <div class="row row-cols-5 g-4 p-4">
                <CharacterItem :character="character" v-for="character in store.characters" />
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
@use '../assets/scss/variables' as *;

.container {
    background-color: $bb-light;

    .found {
        background-color: $bb-darker;

        p {
            color: $bb-light;
        }
    }
}
</style>