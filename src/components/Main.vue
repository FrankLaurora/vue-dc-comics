<template>
    <main>
        <div class="container">
            <h2>--> Content goes here </h2>
        </div>
    </main>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style lang="scss" scoped>
    @import '@/assets/style/variables.scss';
    @import '@/assets/style/common.scss';
    main {
        background-color: $secondary-color;
        color: #fff;
        height: 118px;

        .container {
            align-items: center;
            height: 100%;
        }
    }

</style>