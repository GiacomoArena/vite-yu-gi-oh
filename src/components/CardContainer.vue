
<script>
import {store} from "../data/store";
import Card from "./partials/Card.vue";

export default {
  name:"CardContainer",
  components:{
    Card
    },
    data(){
    return{
      store
    }
  },
}
</script>

<template>
    <section>
      
      <div class="container">
        
        
        <Card v-for="(card, i) in store.resultArray"
        :key="i" 
        :card="card[i]"
        />

      </div>

    </section>
</template>

<style lang="scss" scoped>
  @import '../scss/partials/variables';
  @import '../scss/partials/general' ;
  .container{
    display: flex;
    justify-content: center;
    width: 90%;
    margin: 0 auto;
    background-color: white;
    flex-wrap: wrap;
    span{
      width: 100%;
      height: 60px;
      background-color: $secondary-color;
      color: white;
    }
  }
</style>