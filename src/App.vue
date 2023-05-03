
<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import axios from "axios";  
import {store} from "./data/store";


export default {
  name: "App",
  components:{
    Header,
    Main,
  },
  data(){
    return{
      store
    }
  },
  methods:{
    getApi(){
      store.isLoading = true
      axios.get(store.apiUrl, {
        params:{
          type: store.typeSearch
        }
      })
      .then(result => {
        store.resultArray = result.data;
        //console.log(result.data);


          store.resultArray.data.forEach(element => {
            //console.log(element.type);
            if (!store.listType.includes(element.type)) {
              store.listType.push(element.type)
              store.typeSearch.push(element.type)
            }
          });
          store.isLoading = false
          console.log('listType', store.listType);
            
          
        
      })
    },
    
  },
  mounted(){
    this.getApi();
  }
}

</script>

<template>

  <Header />

  
  <Main @startSearch="getApi" />
  
  

</template>

<style lang="scss">
  @use './scss/main.scss' as * ;
</style>