<template>
  <main>
    <div class="container-main">
      <p>--> Content goes Here  </p>
    </div>
  </main>
</template>

<script>
export default {
  name: 'myMain',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
    @import "../assets/style/variables.scss";
    main {  
        background-color: $Black;
        color : $White;

        .container-main {
            width: 74%;
            margin: auto;
            height: 80px;
            font-size: 21px;
            @include my_row_flex;
        }
    }
</style>