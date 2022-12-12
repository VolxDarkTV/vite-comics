<script>
    export default{
        data(){
            return{
                miniPages: [
                    {
                        text: 'DIGITAL COMICS',
                        img: '../../public/img/buy-comics-digital-comics.png'
                    },
                    {
                        text: 'DC MERCHANDISE',
                        img: '../../public/img/buy-comics-merchandise.png'
                    },
                    {
                        text: 'SUBSCRIPTION',
                        img: '../../public/img/buy-comics-subscriptions.png'
                    },
                    {
                        text: 'COMIC SHOP LOCATOR',
                        img: '../../public/img/buy-comics-shop-locator.png'
                    },
                    {
                        text: 'DC POWER VISA',
                        img: '../../public/img/buy-dc-power-visa.svg'
                    },
                ]
            }
        }
    }
</script>


<template>
    <div class="container">

        <a v-for="(miniPage, index) in miniPages">
            <div>
                <img :src="miniPage.img" alt="#">
            </div>

            <p>{{miniPage.text}}</p>
        </a>

    </div>
</template>


<style lang="scss" scoped>
    .container{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 50px;
        height: 200px;
        background-color: #0282f9;

        & a{
            width: 200px;
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;

            &:hover{
                background-color: #1688f2;
            }

            & div{
                width: 80px;
                height: 80px;
            }
        }
    }
    img{
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
</style>