<template>
    <footer>
        <div class="footer_top">
            <div class="container">
                <div class="small_container">
                    <div class="column">
                        <h3>dc comics</h3>
                        <ul>
                            <li>link 1</li>
                            <li>link 2</li>
                            <li>link 3</li>
                            <li>link 4</li>
                            <li>link 5</li>
                            <li>link 6</li>
                            <li>link 7</li>
                        </ul>
                        <h3>shop</h3>
                        <ul>
                            <li>link 1</li>
                            <li>link 2</li>
                        </ul>
                    </div>
                    <div class="column">
                        <h3>dc</h3>
                        <ul>
                            <li>link 1</li>
                            <li>link 2</li>
                            <li>link 3</li>
                            <li>link 4</li>
                            <li>link 5</li>
                            <li>link 6</li>
                            <li>link 7</li>
                            <li>link 8</li>
                            <li>link 9</li>
                            <li>link 10</li>
                            <li>link 11</li>
                        </ul>
                    </div>
                    <div class="column">
                        <h3>sites</h3>
                        <ul>
                            <li>link 1</li>
                            <li>link 2</li>
                            <li>link 3</li>
                            <li>link 4</li>
                            <li>link 5</li>
                        </ul>
                    </div>
                </div>
                <div class="img_container"></div>
            </div>
        </div>
        <div class="footer_bottom">
            <div class="container">
                <button><a href="#">sign-up now!</a></button>
                <ul>
                    <h3>follow us</h3>
                    <li v-for="(link, index) in social" :key="index">
                        <img :src="require('../assets/img/footer-' + link.name + '.png')" :alt="link.name">
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',

    data() {
        return {
            social: [
                {
                    name: 'facebook',
                },

                {
                    name: 'twitter',
                },

                {
                    name: 'youtube',
                },

                {
                    name: 'pinterest',
                },

                {
                    name: 'periscope',
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/common.scss';
    @import '../assets/style/variables.scss';
    
    .footer_top {
        background-image: url('../assets/img/footer-bg.jpg');
        color: #fff;

        .container {
            justify-content: space-between;

            .small_container {
                display: flex;
                width: calc(100% / 3);
                padding: 45px 0 60px;

                .column {
                    width: calc(100% / 3);

                    h3 {
                        text-transform: uppercase;
                    }
                }
            }

            .img_container {
                width: 44%;
                background-image: url('../assets/img/dc-logo-bg.png');
                background-position: center;
                background-size: cover;
            }
        }
    }

    .footer_bottom {
        background-color: #303030;

        .container {
            justify-content: space-between;
            padding-block: 1.5rem;

            button {
                background-color: transparent;
                border: 1px solid $main-color;
                text-transform: uppercase;
                padding: 0.5rem;

                a {
                    color: #fff;
                    text-decoration: none;
                    font-size: small;
                    font-weight: bold;
                }
            }

            ul {
                display: flex;
                align-items: center;

                h3 {
                    color: $main-color;
                    text-transform: uppercase;
                }

                li {
                    margin-inline: 0.5rem;
                }

                li:last-child {
                    margin-right: 0;
                }
            }
        }
    }

</style>