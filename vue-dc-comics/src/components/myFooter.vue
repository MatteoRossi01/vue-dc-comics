<template>
    <footer>

        <div class="footer-top">
            <div class="footer-left">

                <div class="col">
                    <h2>DC COMICS</h2>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a> 
                </div>

                <div class="col">
                    <h2>DC COMICS</h2>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                </div>

                <div class="col">
                    <h2>DC COMICS</h2>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a> 
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                </div>

                <div class="col">
                    <h2>DC COMICS</h2>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
                    <a href="#">Characters</a>
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

            <div class="footer-social">
                <span>FOLLOW US</span>
                <a href="#">
                    <img src="../assets/img/footer-facebook.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-twitter.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-youtube.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                </a>
                <a href="#">
                    <img src="../assets/img/footer-periscope.png" alt="">
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
    }
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    .footer-top {
        width: 100%;
        height: 260px;
        min-height: 280px;
        background-image: url("../assets/img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        filter: contrast(0.8);
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        position: relative;

        .footer-left {
            margin-top: 15px;
            margin-left: 180px;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;

            .col {
                @include my_col_flex;
                line-height: 20px;
                padding: 0px 25px;

                h2 {
                    color: $White;
                    font-size: 19px;
                    margin-bottom: 5px;
                    margin-top: 15px;
                }

                a {
                    font-size: 11px;
                    text-decoration: none;
                    color: $Grey;
                }
            }  
        }

        .footer-right {
            position: absolute;
            bottom: -58px;
            right: 200px;

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
        justify-content: space-around;

        .footer-btn {
            width: 10%;
            margin-bottom: 10px;

            a {
                text-decoration: none;
                color: $White;
                font-size: 14px;
                font-weight: 500;
                padding: 8px 12px;
                border: 2px solid $Blue;
            }
        }

        .footer-social {
            display: flex;
            flex-direction: row;
            align-items: center;

            span {
                font-size: 18px;
                font-weight: 600;
                color: $Blue;
            }
            
            a {

                img {
                    width: 48px;
                    padding-left: 20px;

                }
            }
        }
    }
</style>