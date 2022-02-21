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
                <li v-for="(link, index) in menuLink" :key="index">
                    <a :class="link.active ? 'active' : ''" href="#">{{link.text}}</a>
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
    },

    data(){

        return {

            menuLink: [

                {
                    text: 'CHARACTERS',
                    active: false,
                },
                {
                    text: 'COMICS',
                    active: true,
                },
                {
                    text: 'MOVIES',
                    active: false,
                },
                {
                    text: 'TV',
                    active: false,
                },
                {
                    text: 'GAMES',
                    active: false,   
                },
                {
                    text: 'COLLECTIBLES',
                    active: false,
                },
                {
                    text: 'VIDEOS',
                    active: false,
                },
                {
                    text: 'FANS',
                    active: false,
                },
                {
                    text: 'NEWS',
                    active: false,
                },
                {
                    text: 'SHOP',
                    active: false,
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";

    .container-header {
        width: 75%;
        height: 80px;
        margin: auto;
        margin-top: 5px;
        @include my_row_flex;
        justify-content: space-between;
        align-items: center;

        .box-logo {
            img {
                width: 60px;
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
                        padding-bottom: 26px;

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
