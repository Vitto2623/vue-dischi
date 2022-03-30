<template>
  <div class="card-box">
      <img :src="CardSong.poster" alt="Album-Image">
      <h3 class="mt-3">{{CardSong.title}}</h3>
      <h5 class="m-0">{{CardSong.author}}</h5>
      <h5 class="m-0">{{CardSong.genre}}</h5>
      <h5>{{CardSong.year}}</h5>
  </div>
</template>

<script>
export default {
    name : 'CardSong',
    props: {
      'CardSong' : Object
    }
}
</script>

<style lang="scss" scoped>
.card-box{
  width: 100%;
  height: 430px;
  padding: 20px;
  background-color: #2e3a46;
  color: white;
  border-radius: 10px;
  box-shadow: 10px 10px 30px black;
  img{
    width: 100%;
  }
  h5{
    color: grey;
  }
}
</style>