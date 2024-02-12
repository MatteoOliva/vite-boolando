<script>
export default {};
</script>

<template>
    <!-- <div class="card"><img src="../assets/img/1.webp" alt="" /></div> -->
</template>

<style lang="scss">
// .card {
//   width: 400px;
//   height: 200px;
//   img {
//     max-width: 100%;
//   }
// }
.container {
  display: flex;
  flex-wrap: wrap;
  width: 60%;
  margin: auto;
  position: relative;

  .card {
    position: relative;
    width: calc(100% / 3);
    flex-grow: 1;
    padding: 10px;
    
    img {
        width: 100%;
    }

    .back-img {
        display: none;
    }
    
  }
  .card:hover {
    .front-img {
        display: none;
    }
    .back-img {
        display: block;
    }
    }
  }

</style>
