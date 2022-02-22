<template>
  <main>
    <div class="container-main">

      <div class="box-img"></div>

      <div class="box-series">

        <span class="current">CURRENT SERIES</span>

        <div class="card-series" v-for="(serie, index) in Series" :key="index">
          <img :src=serie.thumb alt="">
          <div class="box-text-series">
            <span class="title-series">{{serie.series}}</span>
            <span class="genere">{{serie.type}}</span>
            <span class="price">{{serie.price}}</span>
          </div>
        </div>  

        <a href="">LOAD MORE</a>
      </div>

    </div>
  </main>
</template>

<script>
export default {
    name: 'myMain',
    props: {
      msg: String
    },

    data(){

        return {

          Series: [
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
              "price": "$19.99",
              "series": "ACTION COMICS",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
              "price": "$3.99",
              "series": "AMERICAN VAMPIRE 1976",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
              "price": "$16.99",
              "series": "AQUAMAN",
              "type": "Graphic Novel"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
              "price": "$2.99",
              "series": "BATGIRL",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
              "price": "$3.99",
              "series": "BATMAN",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
              "price": "$2.99",
              "series": "BATMAN BEYOND",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
              "price": "$3.99",
              "series": "BATMAN/SUPERMAN",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
              "price": "$4.99",
              "series": "BATMAN/SUPERMAN ANNUAL",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
              "price": "$5.99",
              "series": "BATMAN: THE JOKER WAR ZONE",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
              "price": "$6.99",
              "series": "BATMAN: THREE JOKERS",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
              "price": "$4.99",
              "series": "BATMAN: WHITE KNIGHT PRESENTS: HARLEY QUINN",
              "type": "Comic Book"
            },
            {
              "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
              "price": "$16.99",
              "series": "CATWOMAN",
              "type": "Graphic Novel"
            }
          ]
        }
    }   
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";
    main {  
        background-color: $BackMain;
        color : $White;

        .container-main {
            width: 100%;
            margin: auto;

            .box-img {
              width: 100%;
              height: 310px;
              background-image: url('../assets/img/jumbotron.jpg');
              background-repeat: no-repeat;
              background-size: cover;
            }

            .box-series {
              width: 85%;
              position: relative;
              display: flex;
              justify-content: center;
              flex-direction: row;
              flex-wrap: wrap;
              margin: auto;

              .current {
                font-size: 20px;
                font-weight: 600;
                padding: 7px 12px;
                position: absolute;
                top: -20px;
                left: 20px;
                background-color: $Blue;
              }

              .card-series {
                height: 257px;
                position: relative;
                @include my_col_flex;
                margin-top: 60px;
                padding: 0px 5px;

                img {
                  width: 170px;
                  height: 257px;
                  cursor: pointer;
                }

                .box-text-series {
                  width: 170px;
                  height: 85px;
                  background-color: $BackMain;
                  position: absolute;
                  bottom: 0px;
                  z-index: 3;
                  @include my_col_flex;

                  .title-series {
                    margin-top: 10px;
                    font-size: 15px;
                  }

                  .genere {
                    font-size: 14px;
                    margin-top: 4px;
                    color: $Grey;
                  }

                  .price {
                    color: #EC2D35;
                    font-size: 13px;
                    margin-top: 4px;
                  }
                }
              }

              a {
                text-decoration: none;
                color: #fff;
                font-size: 16px;
                padding: 7px 40px;
                margin-top: 40px;
                margin-bottom: 20px;
                background-color: $Blue;
              }

            }
        }
    }
</style>