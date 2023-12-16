<script>
import axios from 'axios'
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
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Exodia').then((response) => {
            store.cards = response.data
        })
    }
}
</script>
<template>
    <div class="card-container">
        <AppCardTemplate v-for="card in store.cards.data" :name="card.name" :img="card.card_images[0].image_url"
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