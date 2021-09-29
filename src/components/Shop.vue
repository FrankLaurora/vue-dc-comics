<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <img :src="'src/assets/img/' + link.url" :alt="link.name">
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
                    url: 'buy-comics-subscription.png'
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
    @import '@/assets/style/common.scss';
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

            li {
                padding: 50px 42px;
                text-transform: uppercase;
                font-size: small;
            }
        }
    }
</style>