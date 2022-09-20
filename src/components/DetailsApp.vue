<template lang="">
    <div id="details">
         <section class="details d-flex justify-content-center align-items-center" id="sec-3">
            <div class="container">
                <div class="row justify-content-center">
                    <div class="det col-lg-3 rounded-3">
                        <h2 class="text-white">05</h2>
                        <span class="text-white">Clients Order</span>
                    </div>
                    <div class="det col-lg-3 rounded-3 active-card">
                        <h2 class="text-white">03</h2>
                        <span class="text-white">Completed Projects</span>
                    </div>
                    <div class="det col-lg-3 rounded-3">
                        <h2 class="text-white">4.5</h2>
                        <span class="text-white">Stars Rating</span>
                    </div>
                    <div class="det col-lg-3 rounded-3">
                        <h2 class="text-white">12</h2>
                        <span class="text-white">Months Of Experience</span>
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
@import "../sass/main";
.details {
  background-color: $main-color-dark_2;
  padding: 50px 0;
  .row {
    .det {
      cursor: pointer;
      border: 1px dashed $white-color-1;
      height: 180px;
      width: 200px;
      margin: 10px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: $light-dark-color-2;
      &:hover {
        background-color: $main-color;
        border: none;
        transform: scale(1.1);
      }
    }
    .active-card {
      background-color: $main-color;
      border: none;
    }
  }
}
</style>