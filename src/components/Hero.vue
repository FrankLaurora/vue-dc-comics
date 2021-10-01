<template>
    <div class="hero">
        <img :src="path" alt="Jumbotron">
    </div>
</template>

<script>
export default {
    name: 'Hero',

    props: ['path']

}
</script>

<style lang="scss" scoped>
    .hero {
            height: 25rem;
            overflow: hidden;

            img {
                width: 100%;
            }
        }
</style>