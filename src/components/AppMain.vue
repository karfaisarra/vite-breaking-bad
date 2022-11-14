<script>
import CharactersList from './CharactersList.vue'
export default {
    name: 'AppMain',
    components: {
        CharactersList,
    }
}
</script>

<template>
    <main>
        <div class="selectCategory ">
            <select name="" id="" class="p-2 rounded-3">
                <option value="">Select category</option>
            </select>
        </div>
        <CharactersList />
    </main>
</template>

<style lang="scss" scoped>

</style>