<template>
    <div id="view">
     <div class="load-animater" v-if="state.animationStatus">
        <div class="balls">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
        </div>
    </div>
    </div>
</template>

<script>
import { reactive } from 'vue'
export default {
    name: "LoadView",
    setup() {

        const state = reactive({
            animationStatus:true
        })

        function HideAnimater() {
            window.addEventListener("load", () => {
                setTimeout(() => state.animationStatus = false,4000)
            })
        }

        HideAnimater();

        return {
            state,
            HideAnimater
        }
    }
}
</script>

<style lang="scss" scoped>
 @import '../sass/main';

 .load-animater {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  background-color: $dark-color;
  z-index: 10000;
  .balls {
    span {
      width: 100px;
      height: 100px;
      display: block;
      border-radius: 50%;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: $main-color;
    }
    :nth-child(1) {
      animation: anim-1 1s ease-in-out infinite alternate;
      animation-delay: 0.1s;
    }
    :nth-child(2) {
      animation: anim-2 1s ease-in-out infinite alternate;
      animation-delay: 0.2s;
    }
    :nth-child(3) {
      animation: anim-3 1s ease-in-out infinite alternate;
      animation-delay: 0.3s;
    }
    :nth-child(4) {
      animation: anim-4 1s ease-in-out infinite alternate;
      animation-delay: 0.4s;
    }
  }
}
@keyframes anim-1 {
  from {
    transform: translate(-60%, -50%);
  }
  to {
    transform: translate(-90%, -50%);
  }
}
@keyframes anim-2 {
  from {
    transform: translate(-50%, -60%);
  }
  to {
    transform: translate(-50%, -90%);
  }
}
@keyframes anim-3 {
  from {
    transform: translate(-40%, -50%);
  }
  to {
    transform: translate(-10%, -50%);
  }
}
@keyframes anim-4 {
  from {
    transform: translate(-50%, -30%);
  }
  to {
    transform: translate(-50%, -10%);
  }
}
@include media(md) {
  .break {
    display: none;
  }
}
@include media(sm) {
  .break {
    display: none;
  }
}
@include media(xl) {
  .break {
    display: none;
  }
}

</style>