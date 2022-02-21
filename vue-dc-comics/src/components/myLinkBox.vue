<template>
    <div class="container-link-box">

        <div class="link-box">
            <a href="#" class="link-card">
                <div class="box-img">
                    <img src="../assets/img/buy-comics-digital-comics.png" alt="link-img">
                </div>
                <div class="box-txt">
                    <span>DIGITAL COMICS</span>
                </div>
            </a>  

            <a href="#" class="link-card">
                <div class="box-img">
                    <img src="../assets/img/buy-comics-merchandise.png" alt="link-img">
                </div>
                <div class="box-txt">
                    <span>DC MERCHANDISE</span>
                </div>
            </a>  

            <a href="#" class="link-card">
                <div class="box-img">
                    <img src="../assets/img/buy-comics-subscriptions.png" alt="link-img">
                </div>
                <div class="box-txt">
                    <span>SUBSCRIPTIONS</span>
                </div>
            </a>  

            <a href="#" class="link-card">
                <div class="box-img">
                    <img src="../assets/img/buy-comics-shop-locator.png" alt="link-img">
                </div>
                <div class="box-txt">
                    <span>COMIC SHOP LOCATOR</span>
                </div>
            </a>  

            <a href="#" class="link-card">
                <div class="box-img">
                    <img src="../assets/img/buy-dc-power-visa.svg" alt="link-img">
                </div>
                <div class="box-txt">
                    <span>DC POWER VISA</span>
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
    }
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";
    .container-link-box {
        background-color: $Blue;
        position: relative;
        z-index: 2;
      
        .link-box {
            width: 70%;
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