<script>

export default {
    name: 'AddCardTemplate',
    props: ['name', 'img', 'archetype']
}
</script>

<template>
    <div class="card">
        <div class="card-image">
            <img :src="img" :alt="name">
        </div>
        <div class="card-info">
            <h4>{{ name }}</h4>
            <h6>{{ archetype }}</h6>
        </div>
    </div>
</template>1
<style lang="scss" scoped>
.card {

    width: calc((100% / 5) - 16px);

    img {
        width: 100%;
        display: block;
    }

    .card-info {
        background-color: #D48F38;
        padding: 14px;
        height: 100px;

        h4 {
            color: #fff;
            text-transform: uppercase;
            text-align: center;
            font-size: 12px;
            margin-bottom: 6px;
        }

        h6 {
            text-align: center;
            font-weight: 400;
        }

    }

}
</style>