<template>
    <div class="card">
        <div class="img_container">
            <img :src="card.thumb" :alt="card.series">
        </div>
        <p>{{card.series}}</p>        
    </div>
</template>

<script>
export default {
    name: 'Card',

    props: ['card']
}
</script>

<style lang="scss" scoped>
    .card {
        width: calc((100% / 6) - 1rem);
        margin-inline: 0.5rem;
        margin-top: 3rem;

        .img_container {
            width: 100%;
            height: calc((((100vw / 3) * 2) / 6) - 1rem);
            overflow: hidden;
        }

        img {
            display: block;
            width: 100%;
        }
    }

</style>