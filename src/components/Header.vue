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
    <section class="main_container">
        <div class="container">
            <div>
                <img src="../../public/img/dc-logo.png" alt="">
            </div>
    
            <!-- Links -->
            <ul>
                <li v-for="(link, index) in links" :key="index" @click="linkSelect(index)">
                    <a :class="active === index ? 'active' : ''" :href="link.url">{{link.text}}</a>
                    <div class="" :class="active === index ? 'active_under_line' : 'under_line'"></div>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../styles/general.scss' as *;
    .main_container{
        background-color: #fff;
    }
    .container{
        height: 150px;
        display: flex;
        align-items: center;
        justify-content: space-around;
        background-color: #fff;

        // Links
        & ul{
            display: flex;
            gap: 30px;
            list-style: none;
            // effetto under-line
            .under_line{
                width: 0%;
                height: 5px;
            }
            & li:hover .under_line{
                width: 100%;
                background-color: #0282f9;
                transition: all 0.1s ease;
            } 
            // colore testo
            & a{
                text-decoration: none;
                color: #5f7080;
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