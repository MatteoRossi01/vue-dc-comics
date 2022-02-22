<template>
    <div class="container-link-box">

        <div class="link-box">
            <a href="#" class="link-card" v-for="(link, index) in Links" :key="index">
                <div class="box-img">
                    <img :src=link.src alt="link-img">
                </div>
                <div class="box-txt">
                    <span>{{link.text}}</span>
                </div>
            </a>  
        </div>

    </div>
</template>

<script>
export default {
    name: 'myLinkBox',
    props: {
        msg: String
    },

    data(){

        return {

            Links: [

                {
                    text: 'DIGITAL COMICS',
                    src: require('../assets/img/buy-comics-digital-comics.png'),
                },
                {
                    text: 'DC MERCHANDISE',
                    src: require('../assets/img/buy-comics-merchandise.png'),
                },
                {
                    text: 'SUBSCRIPTION',
                    src: require('../assets/img/buy-comics-subscriptions.png'),
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    src: require('../assets/img/buy-comics-shop-locator.png'),
                },
                {
                    text: 'DC POWER VISA',
                    src: require('../assets/img/buy-dc-power-visa.svg'),   
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";
    .container-link-box {
        background-color: $Blue;
        position: relative;
        z-index: 2;
      
        .link-box {
            width: 75%;
            margin: auto;
            height: 100px;
            @include my_row_flex;
            justify-content: space-between;

            .link-card {
                @include my_row_flex;
                justify-content: space-around;
                text-transform: uppercase;
                color: $White;
                font-size: 13px;
                text-decoration: none;

                .box-img {
                    width: 50px;
                    height: 50px;
                    margin-right: 5px;

                    img {
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                    }
                }
            }
        }
    }
</style>