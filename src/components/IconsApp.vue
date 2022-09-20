<template lang="">
    <div id="icons">
        <section class="icons-details" id="sec-5">
            <div class="container text-center">
                <h3 class="title text-white">Why Hire Me</h3>
                <div class="row text-center justify-content-center">
                    <div class="parent col-lg-3 d-flex flex-column align-items-center">
                        <div class="cir  d-flex justify-content-center align-items-center">
                            <div class="roud d-flex justify-content-center align-items-center">
                                <img src="../assets/icons/job.svg" alt="">
                            </div>
                        </div>
                        <div class="text-cont mt-5">
                            <span class="text-white fs-4 text-start">Workaholic</span>
                            <p class="text-lg-start text-light-gray-color-1 mt-4">I’m a kind of person who can’t just
                                stand
                                around and doing nothing. I
                                have
                                a tendency to do
                                something productive.</p>
                        </div>
                    </div>
                    <div class="parent col-lg-3 d-flex flex-column align-items-center">
                        <div class="cir  d-flex justify-content-center align-items-center">
                            <div class="roud d-flex justify-content-center align-items-center">
                                <img src="../assets/icons/mass.svg" alt="">
                            </div>
                        </div>
                        <div class="text-cont mt-5">
                            <span class="text-white fs-4 text-start">Communicative</span>
                            <p class="text-lg-start text-light-gray-color-1 mt-4">I have a broad understanding of verbal
                                vocabulary. Therefore, I can convey a message well to the receiver.</p>
                        </div>
                    </div>
                    <div class="parent col-lg-3 d-flex flex-column align-items-center">
                        <div class="cir  d-flex justify-content-center align-items-center">
                            <div class="roud d-flex justify-content-center align-items-center">
                                <img src="../assets/icons/like.svg" alt="">
                            </div>
                        </div>
                        <div class="text-cont mt-5">
                            <span class="text-white fs-4 text-start">Cooperative</span>
                            <p class="text-lg-start text-light-gray-color-1 mt-4">Behind the successful project, there’s
                                a great team. I can build a good cooperation and remain consistent with the goal.</p>
                        </div>
                    </div>
                    <div class="parent col-lg-3 d-flex flex-column align-items-center">
                        <div class="cir  d-flex justify-content-center align-items-center">
                            <div class="roud d-flex justify-content-center align-items-center">
                                <img src="../assets/icons/done.svg" alt="">
                            </div>
                        </div>
                        <div class="text-cont mt-5">
                            <span class="text-white fs-4 text-start">Perfectionist</span>
                            <p class="text-lg-start text-light-gray-color-1 mt-4">I have a strong intuition. I have
                                remained consistent with high quality standards to present a most worthy result.</p>
                        </div>
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
.icons-details {
  .container {
    .title {
      background-image: url("../assets/logo/text_2.png");
    }
    .row {
      .cir {
        width: 200px;
        height: 200px;
        border-radius: 50%;
        border: 0.5px solid $light-gray-color-1;
        .roud {
          width: 180px;
          height: 180px;
          border-radius: 50%;
          border: 1px solid $main-color;
          background-color: $main-color-dark;
          cursor: pointer;
          &:hover {
            transform: scale(1.2);
          }
        }
      }
    }
  }
}
</style>