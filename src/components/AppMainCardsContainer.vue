<script>
import { store } from '../store';
import AppCardTemplate from './AppCardTemplate.vue';
export default {
    name: 'AppMainCardsContainer',
    components: {
        AppCardTemplate,
    },
    data() {
        return {
            store,
        }
    }
}
</script>
<template>
    <div class="card-container">
        <AppCardTemplate v-for="card in store.cards" :name="card.name" :img="card.card_images[0].image_url"
            :archetype="card.archetype" />
    </div>
</template>

<style lang="scss" scoped>
.card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 20px;
}
</style>