<script>
import { store } from '../store';
export default {
    name: 'AppMainSelectCategoryCard',
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <select name="archetype" id="#archetype-select" v-model="store.selectedArchetype" @change="$emit('search')">
        <option value="">Seleziona l'Archetipo</option>
        <!-- <option v-for="archetype in store.archetypeList" value="{{ archetype.archetype_name }}"> {{ archetype.archetype_name
        }}</option> -->
        <option value="exodia">Exodia</option>
        <option value="alien">Alien</option>
        <option value="dark magician">Dark Magician</option>
        <option value="kuriboh">Kuriboh</option>
        <option value="polymerization">Polymerization</option>

    </select>
</template>
<style scoped>
select {
    border: 1px solid #dddddd;
    padding: 8px 20px;
    border-radius: 4px;
}
</style>