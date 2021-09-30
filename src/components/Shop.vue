<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <img :src="require('../assets/img/' + link.url)" :alt="link.name">
                    {{link.name}}
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Shop',

    data() {
        return {
            links: [
                {
                    name: 'digital comics',
                    url: 'buy-comics-digital-comics.png'
                },

                {
                    name: 'dc merchandise',
                    url: 'buy-comics-merchandise.png'
                },
                
                {
                    name: 'subscription',
                    url: 'buy-comics-subscriptions.png'
                },
                
                {
                    name: 'comic shop locator',
                    url: 'buy-comics-shop-locator.png'
                },
                
                {
                    name: 'dc power visa',
                    url: 'buy-dc-power-visa.svg'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/common.scss';
    section {
        background-color: $main-color;
        color: #fff;

        .container {
            display: flex;
            justify-content: center;
        }

        ul {
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            padding-block: 50px;

            li {
                display: flex;
                align-items: center;
                text-transform: uppercase;
                font-size: small;

                img {
                    height: 55px;
                    margin-right: 1rem;
                }
            }

            li:last-child img {
                height: auto;
                width: 55px;
            }
        }
    }
</style>