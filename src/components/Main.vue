
<script>
import {store} from '../data/store';
import CardContainer from './CardContainer.vue';

export default {
  name:"Main",
  components:{
    CardContainer,
  },
  data(){
    return{
      store
    }
  }
}
</script>

<template>
    <section>



      <select v-model="store.listType"  name="type" id="type">
        <option value= "" >All</option>
        <option v-for="(type, i ) in store.listType" :key="i" :value="type">{{type}}</option>
      </select>

      <button  @click="$emit('startSearch')"> search</button>
      <CardContainer />

    </section>
</template>

<style lang="scss" scoped >
  @import '../scss/partials/variables';
  @import '../scss/partials/general' ;

  section{
    height: 100%;
    background-color: $primary-color;
    select{
      margin: 30px 100px;
      padding: 5px 10px;
      background-color: white;
      border: none;
      cursor: pointer;
    }
  }

</style>