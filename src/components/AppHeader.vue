<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <img src="/yugioh-logo.webp" alt="Yu-Gi-Oh logo">
        <h1>Yu-Gi-Oh Api</h1>
    </header>
</template>
<style scoped>
header {
    padding: 20px;
    display: flex;
    align-items: center;
    gap: 20px;
}

img {
    width: 140px;
}

h1 {
    font-weight: 500;
}
</style>