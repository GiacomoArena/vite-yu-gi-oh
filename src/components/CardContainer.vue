
<script>

import Card from "./partials/Card.vue";

export default {
  name:"CardContainer",
  components:{
    Card
    },
}
</script>

<template>
    <section>

      <div class="container">
      
        <Card />

      </div>

    </section>
</template>

<style lang="scss" scoped>
  @import '../scss/partials/variables';
  @import '../scss/partials/general' ;
  .container{
    width: 90%;
    margin: 0 auto;
    background-color: white;
  }
</style>