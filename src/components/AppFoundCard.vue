<script>
import { store } from '../store';
export default {
    name: 'AppFoundCard',
    props: ['foundCard'],
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="found-card">
        <p v-if="store.cards.length !== 0">{{ foundCard }} carte trovate</p>
        <p v-else>Nessuna carta trovata</p>
    </div>
</template>

<style scoped>
.found-card {
    background-color: #212629;
    color: #fff;
    padding: 16px;
    font-size: 14px;
}
</style>