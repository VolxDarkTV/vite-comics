<script>
    export default{
        data(){
            return{
                active: 0,
                links: [
                    {
                        text: 'CHARACTERS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'COMICS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'MOVIES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'TV',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'GAMES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'COLLECTIBLES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'VIDEOS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'FANS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'NEWS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'SHOP',
                        url: '#',
                        current: false,
                    },
                ]
            }
        },
        methods:{
            linkSelect (index) {    
                let x = index;
                this.active = x;
            },
        }
    }
</script>

<template>
    <div class="container">
        <img src="../../public/img/dc-logo.png" alt="">

        <!-- Links -->
        <ul>
            <li v-for="(link, index) in links" :key="index" @click="linkSelect(index)">
                <a :class="active === index ? 'active' : ''" :href="link.url">{{link.text}}</a>
                <div class="under_line" :class="active === index ? 'active_under_line' : ''"></div>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
    .container{
        height: 150px;
        display: flex;
        align-items: center;
        justify-content: space-around;
        // DEBUG
        background-color: yellow;

        // Links
        & ul{
            display: flex;
            gap: 10px;
            list-style: none;
            // effetto under-line
            & li:hover .under_line{
                background-color: #0282f9;
            } 
            // colore testo
            & a{
                text-decoration: none;
                color: #5f7080;
            }
            .under_line{
                // width: 100%;
                height: 5px;
            }
        }


        // ACTIVE CLASS
        .active{
            color: #0282f9;
        }
        .active_under_line{
            width: 100%;
            height: 5px;
            background-color: #0282f9;
        }
    }
</style>