<script>
    export default{
        data(){
            return{
                links: [
                    {
                        text: 'CHARACTERS'
                    },
                    {
                        text: 'COMICS'
                    },
                    {
                        text: 'MOVIES'
                    },
                    {
                        text: 'TV'
                    },
                    {
                        text: 'GAMES'
                    },
                    {
                        text: 'COLLECTIBLES'
                    },
                    {
                        text: 'VIDEOS'
                    },
                    {
                        text: 'FANS'
                    },
                    {
                        text: 'NEWS'
                    },
                    {
                        text: 'SHOP'
                    },
                ]
            }
        }
    }
</script>

<template>
    <div class="container">
        <img src="../../public/img/dc-logo.png" alt="">

        <!-- Links -->
        <ul>
            <li v-for="(link, index) in links">
                <a href="">{{link.text}}</a>
                <div class="under-line"></div>
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
            & li:hover .under-line{
                background-color: #0282f9;
            } 
            // colore testo
            & a{
                text-decoration: none;
                color: #5f7080;
            }
        }
    }
    .under-line{
        width: 100%;
        height: 5px;
    }
</style>