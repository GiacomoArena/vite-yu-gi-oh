
<script>
export default {
  name:"Header"
}
</script>

<template>
    <div class="top-container">
      <img src="../../public/img/Yu-Gi-Oh!_Logo.webp" alt="logo">
      <h2>yu-gi-oh api</h2>
    </div>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/variables';
  .top-container{
    display: flex;
    align-items: center;
    height: 80px;
    h2{
      text-transform: capitalize;
      display: inline-block;
      font-size: 2rem;
      font-weight: 500;
    }
    img{
      width: 100px;
      margin: 0 15px;
      cursor: pointer;
    }
  }


</style>