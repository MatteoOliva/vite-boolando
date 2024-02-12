<script>
export default {};
</script>

<template>
    <footer>
    <div class="footer-left">
        <p>boolando s.r.l</p>
        <p>informazioni legali informativa sulla privacy</p>
    </div>
    <div class="footer-right">
        <div class="contatti"><p>trovaci anche su</p>
            <i class="fa-brands fa-instagram"></i>
            <i class="fa-brands fa-facebook"></i>
            <i class="fa-brands fa-youtube"></i>
        </div>
        

    </div>
</footer>
    
</template>

<style lang="scss" scoped>
footer {
  width: 100%;
  height: 90px;
  background-color: #1a1a1a;
  margin-top: 100px;
  position: fixed;
  bottom: 0;
  color: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  .footer-right {
    padding-right: 300px;
  }
  .footer-left {
    padding-left: 300px;
  }
}
</style>
