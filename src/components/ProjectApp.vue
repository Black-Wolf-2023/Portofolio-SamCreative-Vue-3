<template>
  <div id="projects">
    <section class="projects" id="sec-4">
      <div class="container">
        <div class="row text-center text-white g-5">
          <h3 class="title">Latest Project</h3>
          <div
            class="cont rounded-3 col-12 flex-column flex-lg-row p-5 d-flex align-items-center justify-content-between bg-dark-color-2"
          >
            <img class="rounded-3" src="../assets/main/1.png" alt />
            <h3 class="my-3 my-lg-0">
              <b class="text-por-1">Soura</b> App
            </h3>
            <button class="btn bg-main-color text-white hover-1">
              <a
                href="https://abdalrhman8000.github.io/Soura_web_lv_4/"
                class="text-white"
                target="_blank"
              >
                View
                Details
              </a>
            </button>
          </div>
          <div
            class="cont rounded-3 col-12 flex-column flex-lg-row p-5 d-flex align-items-center justify-content-between bg-dark-color-2"
          >
            <img class="rounded-3" src="../assets/main/2.png" alt />
            <h3 class="my-3 my-lg-0">
              <b class="text-por-2">Medi</b> site
            </h3>
            <button class="btn bg-main-color text-white hover-1">
              <a
                href="https://abdalrhman8000.github.io/Medisite/"
                class="text-white"
                target="_blank"
              >
                View
                Details
              </a>
            </button>
          </div>
          <div
            class="cont rounded-3 col-12 flex-column flex-lg-row p-5 d-flex align-items-center justify-content-between bg-dark-color-2"
          >
            <img class="rounded-3" src="../assets/main/3.png" alt />
            <h3 class="my-3 my-lg-0">
              <b class="text-por-3">Diago</b> Portofolio
            </h3>
            <button class="btn bg-main-color text-white hover-1">
              <a
                href="https://abdalrhman8000.github.io/Personal_Portfolio_lv_4/"
                class="text-white"
                target="_blank"
              >
                View
                Details
              </a>
            </button>
          </div>
          <div
            class="cont rounded-3 col-12 flex-column flex-lg-row p-5 d-flex align-items-center justify-content-between bg-dark-color-2"
          >
            <div class="text d-flex flex-column align-items-start">
              <h4>Have any project in mind?</h4>
              <p class="text-light-gray-color-1">I’m available for freelancing</p>
            </div>
            <div class="buttons">
              <button
                class="hover-2 w-75 m-auto mt-2 py-2 px-5 btn bg-outline-light-gray-color-2 text-white"
              >More</button>
              <button
                class="hover-1 w-75 m-auto mt-2 justify-content-center p-2 btn bg-primary-color text-white d-flex align-items-center"
              >
                <img class="mx-1" src="../assets/icons/email.svg" alt />
                Email Me
              </button>
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
.title{
  background-image: url("../assets/logo/text.png");
}
.projects {
  overflow-x: hidden;
  .container {
    .row {
      .cont {
        .buttons {
          width: 400px;
          :nth-child(1) {
            &:hover {
              background-color: $main-color !important;
              border: 0;
              color: $white-color-1 !important;
            }
          }
          :nth-child(2) {
            &:hover {
              background-color: transparent !important;
              border: 2px solid $main-color;
            }
          }
        }
      }
    }
  }
}
</style>