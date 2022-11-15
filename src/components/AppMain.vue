<script>
import CharactersList from './CharactersList.vue'
import { store } from '../store.js'
import axios from 'axios'
import SearchSelect from './SearchSelect.vue'

export default {
    name: 'AppMain',
    components: {
        CharactersList,
        SearchSelect
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
            <SearchSelect @searchSelect="searchCategory" />
        </div>
        <CharactersList />
    </main>
</template>

<style lang="scss" scoped>

</style>