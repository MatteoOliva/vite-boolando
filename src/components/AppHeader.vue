<script>
export default {};
</script>

<template>

<header>
      <!--header-left-->
      <div class="header-left"><b>Donna Uomo Bambini</b></div>
      <!--header-center-->
      <div class="header-center">
        <img
          src="../assets/img/boolean-logo.png"
          alt="logo"
          width="130px"
          height="40px"
        />
      </div>
      <!--header-right-->
      <div class="header-right">
        <i class="fa-solid fa-user"></i>
        <i class="fa-regular fa-heart"></i>
        <i class="fa-solid fa-bag-shopping"></i>
      </div>
    </header>

</template>


<style lang="scss" scoped>

header {
  width: 100%;
  height: 70px;
  background-color: #ff6900;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: fixed;
  top: 0;

  .header-left, .header-right {
    color: white;
  }
  .header-right i {
    padding: 5px;
  }
}

</style>
