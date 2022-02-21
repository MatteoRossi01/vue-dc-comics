<template>
    
    <div class="container-header">

        <!-- Logo -->
        <div class="box-logo">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="dc-logo-header">  
            </a>  
        </div>
        <!-- Logo -->

        <!-- Menù -->
        <div class="box-menu">

            <ul>
                <li>
                    <a href="#">CHARACTER</a>
                </li>
                <li>
                    <a href="#">COMICS</a>
                </li>
                <li>
                    <a href="#">MOVIES</a>
                </li>
                <li>
                    <a href="#">TV</a>
                </li>
                <li>
                    <a href="#">GAMES</a>
                </li>
                <li>
                    <a href="#">COLLECTIBLES</a>
                </li>
                <li>
                    <a href="#">VIDEOS</a>
                </li>
                <li>
                    <a href="#">FANS</a>
                </li>
                <li>
                    <a href="#">NEWS</a>
                </li>
                <li>
                    <a href="#">SHOP</a>
                </li>
            </ul>

        </div>
        <!-- Menù -->

    </div>
</template>

<script>
export default{
    name: 'myHeader',
    props: {
        msg: String
    }
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    .container-header {
        width: 75%;
        height: 100px;
        margin: auto;
        margin-top: 5px;
        @include my_row_flex;
        justify-content: space-between;
        align-items: center;

        .box-logo {
            img {
                width: 80px;
            }
        }

        .box-menu {
            width: 65%;
            ul {
                @include my_row_flex;
                justify-content: space-between;
                list-style: none;

                li {
                    a {
                        color: $Black;
                        text-decoration: none;
                        font-size: 13px;
                        font-weight: 700;
                        padding-bottom: 36px;

                        &.active, &:hover{
                            border-bottom: 5px solid $Blue;
                            color:$Blue
                        }
                    }
                }
            }
        }
    }
</style>
