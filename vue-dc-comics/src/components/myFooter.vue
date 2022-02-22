<template>
    <footer>

        <div class="footer-top">
            <div class="footer-left">

                <div class="col" v-for ="(link, index) in footerLinks" :key="index">
                    <h2>{{link.title}}</h2>
                    <span v-for ="(miniLink, index) in link.Links" :key="index">
                        <a href="#">{{miniLink.text}}</a>
                    </span>
                </div>

            </div>

            <div class="footer-right"> 
                <img src="../assets/img/dc-logo-bg.png" alt="footer-logo">
            </div>
        </div>

        <div class="footer-down">
            <div class="footer-btn">
                <a href="#">SIGN-UP NOW!</a>
            </div>
            <span>FOLLOW US</span>
            <div class="footer-social" v-for="(link, index) in socialLinks" :key="index">
                <a href="">
                    <img :src=link.src alt="">
                </a>
            </div>
        </div>

    </footer>
</template>

<script>
export default {
    name: "myFooter",
    props: {
        msg: String
    },

    data(){

        return {

            footerLinks: [

               {
                    title: 'DC COMICS',

                    Links: [
                        {
                        text:'Characters',        
                        },
                        {
                        text:'Comics',        
                        },
                        {
                        text:'Movies',   
                        },
                        {
                        text:'Tv',
                        },
                        {
                        text:'Games',                        
                        },
                        {
                        text:'Videos',  
                        },
                        {
                        text:'News',
                        },
                    ],
                },

                {
                    title: 'SHOP',

                    Links: [
                        {
                        text:'Shop DC',        
                        },
                        {
                        text:'Shop DC Collectibles',        
                        },
                    ],
                },

                {
                    title: 'DC',

                    Links: [
                        {
                        text:'Term Of Use',        
                        },
                        {
                        text:'Privacy policy(new)',        
                        },
                        {
                        text:'Ad Choices',   
                        },
                        {
                        text:'Addvertising',
                        },
                        {
                        text:'Jobs',                        
                        },
                        {
                        text:'Subscriptions',  
                        },
                        {
                        text:'Talent Workshop',
                        },
                        {
                        text:'CPSC Certificates',
                        },
                        {
                        text:'Ratings',                        
                        },
                        {
                        text:'Shop Help',  
                        },
                        {
                        text:'Contact Us',
                        },
                    ],
                },

                {
                    title: 'SITES',

                    Links: [
                        {
                        text:'DC',        
                        },
                        {
                        text:'MAD Magazine',        
                        },
                        {
                        text:'DC Kids',                        
                        },
                        {
                        text:'DC Universe',  
                        },
                        {
                        text:'DC Power Visa',
                        },
                    ],
                },
            ],

            socialLinks: [

                {
                    src: require('../assets/img/footer-facebook.png'),
                },
                {
                    src: require('../assets/img/footer-twitter.png'),
                },
                {
                    src: require('../assets/img/footer-youtube.png'),
                },
                {
                    src: require('../assets/img/footer-pinterest.png'),
                },
                {
                    src: require('../assets/img/footer-periscope.png'),   
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    .footer-top {
        width: 100%;
        height: 272px;
        background-image: url("../assets/img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        filter: contrast(0.8);
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        position: relative;

        .footer-left {
            margin-top: 10px;
            margin-left: 150px;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;

            .col {
                @include my_col_flex;
                line-height: 17px;
                padding: 0px 25px;

                h2 {
                    color: $White;
                    font-size: 19px;
                    margin-bottom: 5px;
                    margin-top: 15px;
                }

                a {
                    font-size: 12px;
                    text-decoration: none;
                    color: $Grey;
                }
            }  
        }

        .footer-right {
            position: absolute;
            bottom: -58px;
            right: 165px;

            img {
                width: 400px;
            }
        }
    }

    .footer-down {
        background-color: $DarkGrey;
        height: 80px;
        position: relative;
        z-index: 2;
        display: flex;
        align-items: center;

        .footer-btn {
            width: 10%;
            margin-bottom: 10px;
            position: absolute;
            left: 170px;

            a {
                text-decoration: none;
                color: $White;
                font-size: 14px;
                font-weight: 500;
                padding: 8px 12px;
                border: 2px solid $Blue;
            }
        }

        span {
            font-size: 18px;
            font-weight: 600;
            color: $Blue;
            position: absolute;
            right: 425px;
        }

        .footer-social {
            display: flex;
            align-items: center;
            position: relative;
            left: 945px;

            a {
                img {
                    width: 48px;
                    padding-left: 19px;
                }
            }
        }
    }
</style>