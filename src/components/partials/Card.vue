
<script>
import {store} from "../../data/store";

export default {
  name:"Card",

  props:{
    card: Object,
    type:String
  },
  data(){
    return{
      store,
    }
  },
  methods:{
    
  },
  mounted(){
    console.log(this.card);
  }
}
</script>

<template>

  <div class="card-container">
    <img  :src="card.card_images[0].image_url" alt="card">
    <div class="card-info">
      <h5>	{{card.name}}</h5>
      <span>{{type}}</span>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>
  @import '../../scss/partials/variables';
  @import '../../scss/partials/general';
  .card-container{
    width: calc(100% / 6);
    margin: 20px 10px;
    flex-wrap: wrap;
    text-align: center;
    img{
      width: 100%;
    }
    h5{
      font-size: 1rem;
      padding: 15px 0;
    }
    .card-info{
      width: 100%;
      height: 130px;
      background-color: $primary-color;
    }
  }
</style>