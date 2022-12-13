<script>

    // Import SignUp
    import SignUp from './SignUp.vue'


    export default{
        components:{
            SignUp,
        },
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
                ],
                DcShops:[
                    {
                        text: 'SHOP DC',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'SHOP DC COLLECTIBLES',
                        url: '#',
                        current: false,
                    },
                ],
                DcLinks:[
                    {
                        text: 'TERMS OF USE',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'PRIVACY POLICY (NEW)',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'AD CHOICES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'ADVERTISING',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'JOBS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'SUBSCRIPTIONS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'TALENT WORKSHOPS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'CSPC CERTIFICATES',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'RATINGS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'SHOP HELP',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'CONTACT US',
                        url: '#',
                        current: false,
                    },
                ],
                sites:[
                    {
                        text: 'DC',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'MAD',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'MAGAZINE',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'DC KIDS',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'DC UNIVERSE',
                        url: '#',
                        current: false,
                    },
                    {
                        text: 'DC POWER VISA',
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
    <section class="background">
        <section class="container">
            <div class="logo"></div>
    
            <div class="left_side">
                <div>
                    <ul>
                        <h4>DC COMICS</h4>
                        <li v-for="(link, index) in links" :key="index" @click="linkSelect(index)">
                            <a :class="active === index ? 'active' : ''" :href="link.url">{{link.text}}</a>
                            <div class="under_line" :class="active === index ? 'active_under_line' : ''"></div>
                        </li>
                    </ul>
                    <ul>
                       <h4>SHOP</h4>
                       <li v-for="(DcShop, index) in DcShops" :key="index">
                            <a :href="DcShop.url">{{DcShop.text}}</a>
                       </li>
                    </ul>
                </div>
                <ul>
                    <h4>DC</h4>
                    <li v-for="(DcLink, index) in DcLinks" :key="index">
                        <a :href="DcLink.url">{{DcLink.text}}</a>
                    </li>
                </ul>
                <ul>
                    <h4>SITES</h4>
                    <li v-for="(site, index) in sites" :key="index">
                        <a :href="site.url">{{site.text}}</a>
                    </li>
                </ul>
            </div>
    
            <SignUp/>
        </section>
    </section>

</template>

<style lang="scss" scoped>
    @use '../styles/general.scss' as *;
    .background{
        position: relative;
        width: 100vw;
        height: 100vh;
        background-image: url(../../public/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
    }
    .logo{
        position: absolute;
        right: 0px;
        top: -100px;
        width: 50vw;
        height: 90vh;
        background-image: url(../../public/img/dc-logo-bg.png);
        background-repeat: no-repeat;
    }
    .left_side{
        display: flex;
        justify-content: center;
        gap: 50px;
        width: 50%;
    }

    // Links
    ul{
        // gap: 30px;
        list-style: none;
        // colore testo
        & h4{
            margin: 20px 0;
            font-size: 20px;
            font-weight: 900;
        }
        & a{
            text-decoration: none;
            color: #5f7080;
            font-size: 14px;

            &:hover{
                text-decoration: underline;
                color: #7e8b97;
            }
        }
      }
</style>