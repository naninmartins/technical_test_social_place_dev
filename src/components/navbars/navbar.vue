<template>
  <div class="row container-fluid border-bottom">

    <grid-vue :size="{col:[1,1,1],offset:[5,0,0], opts:''}">
      <a class="navbar-brand" :href="url">
        <img v:if="" :src="img" :width="imgWidth" :height="imgHeight" class="d-inline-block align-top" alt="">
      </a>
    </grid-vue>

    <grid-vue v-if="$store.getters.getSizeScreen != 'sm'" :size="{col:[8,5,4],offset:[2,5,5], opts:'navbar'}">
      <input-search/>
    </grid-vue>
          
    <grid-vue v-if="$store.getters.getSizeScreen == 'lg'" :size="{col:[2,2,2],offset:[0,0,0], opts:'btn btn-group navbar'}">
      <button @click="notDeveloped" :class="buttonBoostrapStyle" >
        <i class="fas fa-user fa-lg" @click="notDeveloped"></i> 
      </button>    
      <button @click="notDeveloped" :class="buttonBoostrapStyle" >
        <i class="fas fa-user-cog fa-lg" @click="notDeveloped"></i> 
      </button> 
    </grid-vue>
    
  </div>
  
</template>

<script>
// @ is an alias to /src
export default {
  name: 'NavBar',
  props:['img','imgWidth','imgHeight','url','cor'],
  data () {
    return {
      message : "",
      buttonBoostrapStyle : "btn btn-outline-dark btn-lg border-0 rounded"
    }
  },
  methods: {
    notDeveloped: function () {
      return alert('Desculpe, função ainda em desenvolvimento!');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">


</style>
