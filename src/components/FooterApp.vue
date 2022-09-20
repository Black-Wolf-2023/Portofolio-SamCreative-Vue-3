<template lang="">
    <div id="footer">
        <footer>
            <div class="container">
                <h2 class="text-white">Get in Touch</h2>
                <p class="text-light-gray-color-1 mt-5">For business and partnership inquiry please contact me below!
                </p>
                <div class="contact">
                    <div class="content d-flex  align-items-center my-4">
                        <div class="icon"><img src="../assets/icons/fluent_call-20-filled.svg" alt=""></div>
                        <div class="text">
                            <p class="m-0 text-light-gray-color-1">Phone</p>
                            <p class="m-0 text-white">0899-3415-875</p>
                        </div>
                    </div>
                    <div class="content d-flex  align-items-center my-4">
                        <div class="icon"><img src="../assets/icons/eva_email-fill.svg" alt=""></div>
                        <div class="text">
                            <p class="m-0 text-light-gray-color-1">Email</p>
                            <p class="m-0 text-white">dimasarsmith@gmail.com</p>
                        </div>
                    </div>
                    <div class="content d-flex  align-items-center my-4">
                        <div class="icon"><img src="../assets/icons/fluent_location-48-filled.svg" alt=""></div>
                        <div class="text">
                            <p class="m-0 text-light-gray-color-1">Address</p>
                            <p class="m-0 text-white">Griya Japan Raya Tahap 4 B2/01, Sooko, Mojokerto</p>
                        </div>
                    </div>
                </div>
            </div>
        </footer>
    </div>
</template>
<script>
export default {};
</script>
<style lang="scss">
@import "../sass/rest";
footer {
  margin-top: 150px;
  background: url("../assets/main/footer.png");
  background-position: bottom right;
  .container {
    .contact {
      .content {
        .icon {
          width: 40px;
          height: 40px;
          border-radius: 50%;
          border: 1px solid $white-color-1;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-right: 20px;
        }
      }
    }
  }
}
</style>