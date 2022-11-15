<script>
import CharactersList from './CharactersList.vue'
import { store } from '../store.js'
import axios from 'axios'

export default {
    name: 'AppMain',
    components: {
        CharactersList,
    },
    data() {
        return {
            store
        }
    },
    methods: {
        searchCategory() {
            const category = this.store.category
            const url = `${this.store.API_URL}?category=${category}`
            axios.get(url)
                .then(response => {
                    this.store.characters = response.data

                })
                .catch(err => {
                    console.log(err);
                })
        }
    }
}
</script>

<template>
    <main>
        <div class="container py-4">
            <div class="selectCategory ">
                <select class="p-2 rounded-3" v-model="store.category" @change="searchCategory">
                    <option value="">Select category</option>
                    <option value="Breaking Bad">Breaking Bad</option>
                    <option value="Better Call Saul">Better Call Saul</option>
                </select>
            </div>
        </div>
        <CharactersList />
    </main>
</template>

<style lang="scss" scoped>

</style>