<script>
import SelectCategoy from './SelectCategoy.vue';
import CharactersList from './CharactersList.vue'
export default {
    name: 'AppMain',
    components: {
        SelectCategoy,
        CharactersList,
    }
}
</script>

<template>
    <main>
        <SelectCategoy />
        <CharactersList />
    </main>
</template>

<style lang="scss" scoped>

</style>