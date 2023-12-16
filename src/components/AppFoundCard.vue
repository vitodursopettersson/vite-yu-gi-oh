<script>
import { store } from '../store';
export default {
    name: 'AppFoundCard',
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div class="found-card">

        <p>Found {{ store.cards.data.length }} cards</p>
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