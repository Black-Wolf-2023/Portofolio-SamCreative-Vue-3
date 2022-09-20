<template>
  <div id="offer">
    <section class="offer container" id="sec-2">
      <div class="row justify-content-center align-items-center text-center">
        <div class="head col-lg-7 d-flex flex-column justify-content-center align-items-center">
          <span class="text-light-gray-color-1">What Do I Offer</span>
          <h2 class="text-white lh-base">
            Creates Professional Design That’s
            Oriented Towards Client Needs
          </h2>
          <div class="bg-main-color line rounded-3"></div>
          <div class="scroller d-flex justify-content-center mt-5 w-100 gap-3">
            <div class="img rounded-3" :class="[active == 0 ? 'active-img':'']" @click="activer(0)" >
              <img src="../assets/main/Picsart_2.png" alt />
              <span class="text-main-color">Content Design</span>
            </div>
            <div class="img rounded-3" :class="[active == 1 ? 'active-img':'']" @click="activer(1)" >
              <img src="../assets/main/Picsart.png" alt />
              <span class="text-main-color">Mobile App Design</span>
            </div>
            <div class="img rounded-3" :class="[active == 2 ? 'active-img':'']" @click="activer(2)" >
              <img src="../assets/main/Picsart_3.png" alt />
              <span class="text-main-color">Web Design</span>
            </div>
          </div>
          <div class="scroll-conrolls d-flex justify-content-center align-items-center gap-3">
            <div @click="activer(index)" class="liner bg-light-gray-color-1 rounded-3" v-for="(line,index) in lines" :key="index" :class="[index == active ? 'active-img-line':'']"></div>
            <!-- <div class="liner bg-light-gray-color-1 active-img-line rounded-3"></div>
            <div class="liner bg-light-gray-color-1 rounded-3"></div> -->
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
    name: "OfferApp",
    data() {
        return {
          active: 1,
            lines:[1,2,3]
        }
    },
    methods: {
        activer(index) {
            this.active = index;
      }

  }
};
</script>

<style lang="scss">
@import "../sass/main";
.offer {
  .row {
    margin-bottom: 50px;

    .head {
      .line {
        width: 300px;
        height: 7px;
        margin-top: 60px;
      }

      .scroller {
        .img {
          overflow: hidden;
          height: 250px;
          border: 1px solid $main-color;
          background-color: $main-color-dark;
          position: relative;
          cursor: pointer;
          transform: scale(0.8);

          &::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: transparent;
            backdrop-filter: blur(2px);
          }
        }

        .active-img {
          transform: scale(1);

          &::after {
            backdrop-filter: blur(0px);
          }
        }
      }

      .scroll-conrolls {
        height: 60px;
        margin-top: 50px;
        cursor: pointer;

        .liner {
          width: 50px;
          height: 7px;
        }

        .active-img-line {
          background-color: $main-color !important;
        }
      }
    }
  }
}

@include media(md) {
  .offer {
    .row {
      margin-top: 600px;
    }
  }
}

@include media(sm) {
  .offer {
    .row {
      margin-top: 500px;

      .head {
        .scroller {
          .img {
            height: 150px;
            width: 150px;
            padding: 15px;

            span {
              font-size: 14px;
            }
          }
        }
      }
    }
  }
}

@include media(xl) {
  .offer {
    .row {
      margin-top: 500px;

      .head {
        .scroller {
          .img {
            height: 150px;
            width: 150px;
            padding: 5px;

            span {
              font-size: 14px;
            }
          }
        }
      }
    }
  }
}
</style>