<script>
import AppMainSelectCategoryCard from './AppMainSelectCategoryCard.vue';
import AppFoundCard from './AppFoundCard.vue';
import AppMainCardsContainer from './AppMainCardsContainer.vue';

export default {
    name: 'AppMain',
    components: {
        AppMainSelectCategoryCard,
        AppFoundCard,
        AppMainCardsContainer,
    }
}
</script>

<template>
    <main>
        <div class="container">
            <AppMainSelectCategoryCard />
            <div class="container-groupcard">
                <AppFoundCard />
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