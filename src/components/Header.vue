<template>
  <div class="container-fluid my-header">
      <div class="row">
          <div class="col-6">
              <img src="https://media.ilsoftware.it/images/500x500/img_19519.jpg" alt="logo-spotify" class="p-2">
          </div>
          <div class="col-6 d-flex justify-content-end align-items-center pe-4">
              <select name="generi-musicali" class="h-50">
                  <option value="rock">Rock</option>
                  <option value="pop">Pop</option>
                  <option value="jazz">Jazz</option>
                  <option value="metal">Metal</option>
              </select>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style lang="scss" scoped>
.my-header{
    height: 8vh;
    width: 100%;
    background-color: black;
    img{
        height: 8vh;
    }
}
</style>