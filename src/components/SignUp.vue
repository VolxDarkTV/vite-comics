<script>
    export default{
        data(){
            return{
                socials:[
                    {
                        img: '../../public/img/footer-facebook.png',
                        url: '#'
                    },
                    {
                        img: '../../public/img/footer-twitter.png',
                        url: '#'
                    },
                    {
                        img: '../../public/img/footer-youtube.png',
                        url: '#'
                    },
                    {
                        img: '../../public/img/footer-pinterest.png',
                        url: '#'
                    },
                    {
                        img: '../../public/img/footer-periscope.png',
                        url: '#'
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="total_container">
        <div class="container internal_container">
            <div id="sign_up">
                <h4>SIGN-UP NOW!</h4>
            </div>
            <div id="socials">
                <div>
                    <h3>FOLLOW US</h3>
                </div>
                <ul>
                    <li v-for="(social, index) in socials" :key="index">
                        <a :href="social.url">
                            <img :src="social.img" alt="">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../styles/general.scss' as *;
    .total_container{
        display: flex;
        align-items: center;
        justify-content: center;
        position: fixed;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 150px;
        background-color: #303030;
    }
    .internal_container{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 80%;
    }
    #sign_up{
        border: #0282f9 solid 2px;
        padding: 12px;
        cursor: pointer;

        &:hover{
            border: #fff solid 2px;

        }
    }
    #socials{
        display: flex;
        align-items: center;
        gap: 20px;

        & div{
            color: #0282f9;
        }
        
        & ul{
            display: flex;
            gap: 20px;
            list-style: none;
        }
    }
</style>