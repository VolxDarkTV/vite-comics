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
                       <li>
                            <a href="">SHOP DC</a>
                       </li>
                       <li>
                            <a href="">SHOP DC COLLECTIBLES</a>
                       </li>
                    </ul>
                </div>
                <ul>
                    <h4>DC</h4>
                    <li>
                        <a href="">TERMS OF USE</a>
                    </li>
                    <li>
                        <a href="">PRIVACY POLICY (NEW)</a>
                    </li>
                    <li>
                        <a href="">AD CHOICES</a>
                    </li>
                    <li>
                        <a href="">ADVERTISING</a>
                    </li>
                    <li>
                        <a href="">JOBS</a>
                    </li>
                    <li>
                        <a href="">SUBSCRIPTIONS</a>
                    </li>
                    <li>
                        <a href="">TALENT WORKSHOPS</a>
                    </li>
                    <li>
                        <a href="">CPSC CERTIFICATES</a>
                    </li>
                    <li>
                        <a href="">RATINGS</a>
                    </li>
                    <li>
                        <a href="">SHOP HELP</a>
                    </li>
                    <li>
                        <a href="">CONTACT US</a>
                    </li>
                </ul>
                <ul>
                    <h4>SITES</h4>
                    <li>
                        <a href="">DC</a>
                    </li>
                    <li>
                        <a href="">MAD MAGAZINE</a>
                    </li>
                    <li>
                        <a href="">DC KIDS</a>
                    </li>
                    <li>
                        <a href="">DC UNIVERSE</a>
                    </li>
                    <li>
                        <a href="">DC POWER VISA</a>
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
        gap: 20px;
        width: 50%;
    }

    // Links
    ul{
        gap: 30px;
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

            &:hover{
                text-decoration: underline;
                color: #7e8b97;
            }
        }
      }
</style>