<script>
import { store } from '../store.js';
export default {
    name: 'SearchSelect',
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="selectCategory">
        <select class="form-select w-25 p-2 rounded-3" v-model="store.category" @change="searchCategory">
            <option value="">Select category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Better Call Saul">Better Call Saul</option>
        </select>
    </div>
</template>
<style>

</style>