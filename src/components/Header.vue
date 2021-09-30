<template>
    <header>
        <div class="container">
            <img src="../assets/img/dc-logo.png" alt="DC comics logo">
            <ul>
                <li v-for="(link, index) in links" :key="index" :class="{ active : link.active }">{{link.name}}</li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',

    data() {
        return {
            links: [
                {
                    name: 'characters',
                    url: '#', 
                    active: false
                },

                {
                    name: 'comics',
                    url: '#', 
                    active: true
                },
                
                {
                    name: 'movies',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'tv',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'games',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'collectibles',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'videos',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'fans',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'news',
                    url: '#', 
                    active: false
                },
                
                {
                    name: 'shop',
                    url: '#', 
                    active: false
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/common.scss';

    header {

        .container {
            justify-content: space-between;
            align-items: center;
        }

        ul {
            display: flex;

            li {
                list-style: none;
                padding: 3.2rem 1rem;
                text-transform: uppercase;
                color: #464646;
                font-size: small;
                font-weight: bold;

                &.active {
                    color: $main-color;
                    border-bottom: 5px solid $main-color;
                }
            }
        }
    }
</style>