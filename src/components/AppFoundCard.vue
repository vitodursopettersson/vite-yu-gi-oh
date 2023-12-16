<script>
export default {
    name: 'AppFoundCard',
    props: ['foundCard']
}
</script>

<template>
    <div class="found-card">
        <p>Found {{ foundCard }} cards</p>
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