<template>
  <div id="tools">
    <section class="tools" id="sec-6">
      <div class="container text-center">
        <h3 class="title text-white">Tools and Skills</h3>
        <div class="row justify-content-center">
          <div class="img">
            <img src="../assets/main/psd.png" alt />
          </div>
          <div class="img">
            <img src="../assets/main/figma.png" alt />
          </div>
          <div class="img">
            <img src="../assets/main/html.png" alt />
          </div>
          <div class="img">
            <img src="../assets/main/css.png" alt />
          </div>
          <div class="img">
            <img src="../assets/main/xml.png" alt />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
@import "../sass/rest";
.tools {
  .container {
    .row {
      .img {
        width: 200px;
        &:hover {
          transform: scale(1.1);
          cursor: pointer;
        }
      }
    }
  }
}
</style>