
<script>

import CardContainer from './CardContainer.vue';

export default {
  name:"Main",
  components:{
    CardContainer,
  },
  data(){
    return{

    }
  }
}
</script>

<template>
    <section>

      <label for="type"></label>
      <select name="type" id="type">
        <option value="alien">alien</option>
        <option value="monster">monster</option>
      </select>

      <CardContainer />

    </section>
</template>

<style lang="scss" scoped >
  @import '../scss/partials/variables';
  @import '../scss/partials/general' ;

  section{
    height: 100vh;
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