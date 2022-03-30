<template>
    <main class="container-fluid my-container">
      <div class="row justify-content-center">
        <div v-for="(element, index) in main" :key="index" class="col-2 mb-4 me-1 text-center">
          <CardSong :CardSong="element"/>
        </div>
      </div>
    </main>
</template>

<script>
import CardSong from "./CardSong.vue";
import axios from "axios";
export default {
  name: "Main",
  components: {
    CardSong,
  },
  data: function(){
    return{
      main : null,
    }
  },
  created: function(){
    this.getApiMusic();
  },
  methods: {
    getApiMusic(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result) =>{
        this.main = result.data.response;
        console.log(this.main);
      })
      .catch((error)=>{
        console.error(error)
      })
    }
  }
};
</script>

<style lang="scss" scoped>
.my-container{
  background-color: #1e2d3b;
  width: 100%;
  padding: 230px;
}
</style>