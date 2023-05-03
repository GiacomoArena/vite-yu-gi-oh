
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
  mounted(){
  }
}
</script>

<template>
    <section>
      
      <div class="container">

        <div class="filter-container">
          <h1 v-if="store.resultArray.length != 0"> Found {{store.resultArray.data.length}} Cards</h1>          
          <h1 v-else> Found {{store.resultArray.length}} Cards</h1>          
        </div>
        
        <Card v-for="(card, index) in store.resultArray.data"
        :key="index" 
        :card="card"
        :type="card.type"
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
    
    .filter-container{
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 80px;
      background-color: $secondary-color;
      margin-top: 20px;
      color: $primary-color;
    }
    h1{
      
    }
  }
</style>