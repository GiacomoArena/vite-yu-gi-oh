
<script>
import {store} from '../data/store';
import CardContainer from './CardContainer.vue';
import Loading from '../components/partials/Loading.vue';

export default {
  name:"Main",
  components:{
    CardContainer,
    Loading
  },
  data(){
    return{
      store
    }
  },
  methods:{
    reset(){
      store.listType =[]
      store.typeSearch =[]
    }
  }
}
</script>

<template>
    <section>



      <select @click="$emit('startSearch')" v-model="store.typeSearch"  name="type" id="type">
        <option value='' @click="reset()" >All</option>
        <option v-for="(type, i ) in store.listType" :key="i" :value="type">{{type}}</option>
      </select>

      <Loading 
      v-if="store.isLoading"
      />

      <CardContainer 
      v-else
      />

    </section>
</template>

<style lang="scss" scoped >
  @import '../scss/partials/variables';
  @import '../scss/partials/general' ;

  section{
    min-height: 100vh;
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