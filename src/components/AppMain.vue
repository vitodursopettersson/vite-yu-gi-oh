<script>
import axios from 'axios'
import { store } from '../store';
import AppMainSelectCategoryCard from './AppMainSelectCategoryCard.vue';
import AppFoundCard from './AppFoundCard.vue';
import AppMainCardsContainer from './AppMainCardsContainer.vue';

export default {
    name: 'AppMain',
    components: {
        AppMainSelectCategoryCard,
        AppFoundCard,
        AppMainCardsContainer,
    },
    data() {
        return {
            store,
        }
    },
    methods: {
        searchArchetype() {
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=Exodia', {
                params: {
                    archetype: store.selectedArchetype
                }
            }).then((response) => {
                store.cards = response.data.data
            })
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php').then((response) => {
            store.archetypeList = response.data
        })
    }

}
</script>

<template>
    <main>
        <div class="container">
            <AppMainSelectCategoryCard @search="searchArchetype" />
            <div class="container-groupcard">
                <AppFoundCard :foundCard="store.cards.length" />
                <AppMainCardsContainer />
            </div>
        </div>
    </main>
</template>
<style scoped>
main {
    background-color: #D48F38;
}

.container-groupcard {
    background-color: #fff;
    padding: 20px;
    margin-top: 20px;
    border-radius: 4px;
}
</style>