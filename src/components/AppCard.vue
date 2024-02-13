<script>
export default {};
</script>

<template>
  <!-- <div class="card"><img src="../assets/img/1.webp" alt="" /></div> -->
</template>

<style lang="scss">
@use '../styles/partials/variables.scss' as *;
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
  .wishlist {
    position: absolute;
    top: 1rem;
    right: 0;
    width: 45px;
    height: 45px;
    line-height: 45px;
    text-align: center;
    background-color: white;
    
    &:hover {
        color: $primary-color;
    }
  }
  .img-content {
  position: absolute;
  top: 76%;
  width: 150px;
  height: 30px;
}
.red-font {
  color: $primary-color;
}
.red-fontt {
  color: white;
  background-color: $primary-color;
}
.green-font {
  color: white;
  align-items: center;
  background-color: $secondary-color;
}
}
</style>
