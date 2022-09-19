<template>
    <div id="hero">
         <section class="hero container" id="sec-1">
            <div class="row h-100">
                <div class="info col-lg-6 h-100 d-flex flex-column justify-content-center">
                    <h3 class="text-white">Hello Sur</h3>
                    <h1 class="text-white">I am <span class="text-main-color type">{{state.letter}}</span></h1>
                    <span class="text-light-gray-color-2">UI / UX Design Enthusiast</span>
                    <hr class="bg-light-gray-color-2" style="height: 4px; width: 60px;">
                    <p class="text-light-gray-color-2">I'm a person who has a keen interest in the design layout. I
                        think presenting an attractive
                        design is a matter of concern in developing a branding of products. To creates a good
                        design, I focus on proper composition and visual decoration details in order to make it more
                        professional. For the time being, I’m developing the skill for acquiring the UI/UX design
                        for dynamic application and web development.</p>
                    <div class="buttons w-100 d-flex gap-3">
                        <button class="p-2 btn bg-primary-color text-white"><img class="mx-1"
                                src="../assets/icons/subtract.svg" alt="">
                            Download CV</button>
                        <button class="py-2 px-5 btn bg-outline-light-gray-color-2 text-white">More</button>
                    </div>
                </div>
                <div class="social col-lg-6 d-flex gap-3 align-items-end justify-content-evenly flex-column">
                    <div class="img">
                        <img src="../assets/person/person.png" alt="">
                    </div>
                    <div class="social_links d-flex gap-4 align-items-center  w-100 justify-content-center">
                        <h6 class="text-white m-0">Find Me On</h6>
                        <span class="rounded-circle bg-main-color-dark"><img width="18px" height="18px"
                                src="../assets/icons/bxl_facebook.svg" alt=""></span>
                        <span class="rounded-circle bg-main-color-dark"><img width="18px" height="18px"
                                src="../assets/icons/instagram.svg" alt=""></span>
                        <span class="rounded-circle bg-main-color-dark"><img width="18px" height="18px"
                                src="../assets/icons/whatsapp.svg" alt=""></span>
                        <span class="rounded-circle bg-main-color-dark"><img width="18px" height="18px"
                                src="../assets/icons/linkedin.svg" alt=""></span>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>
<script>
import { reactive} from 'vue';
export default {
    name: "HeroApp",
    setup() {
        const state = reactive({
            index: 0,
            start: 0,
            data: ['Abdalrahman Eldip', 'Front End Developer', 'And Ui/Ux', 'Disgner'],
            word: '',
            letter:''
        })
    // setTimeout(() => {
    // typingFun();
    // },4500)


    function typingFun(){
        state.word   = state.data[state.index]
        state.letter = state.word.slice(0,state.start++);

        if(state.index == state.data.length-1)
        {
            state.index = 0 
        }

        if(state.word.length == state.letter.length)
        {
            state.start = 0;
            state.index++;
        }

        state.letter;

        setTimeout(typingFun, 230);
    }
    
    typingFun()
        return {
            state,
            typingFun,
        }
    }
}
</script>


<style lang="scss" scoped>
@import '../sass/main';
.hero {
  height: calc(90vh - 78px);
}
.social {
  .img {
    width: 400px;
  }
  .social_links {
    span {
      width: 35px;
      height: 35px;
      display: flex;
      justify-content: center;
      align-items: center;
      &:hover {
        background-color: $light-color-2 !important;
        cursor: pointer;
        transform: scale(1.2);
      }
    }
  }
}
.type {
  position: relative;
}
.type::after {
  content: "";
  width: 2px;
  height: 90%;
  position: absolute;
  background-color: $main-color;
  animation: opacity 0.4s ease forwards infinite;
}
@keyframes opacity {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
.buttons {
  :nth-child(1) {
    &:hover {
      background-color: transparent !important;
      border: 2px solid $main-color;
      color: $main-color !important;
    }
  }
  :nth-child(2) {
    &:hover {
      background-color: $main-color !important;
      border: none;
    }
  }
}
@include media(sm) {
  .social {
    .img {
      width: 100%;
      padding-left: 40px;
    }
  }
}
@include media(xl) {
  .hero {
    padding-top: 90px;
  }
  .social {
    .img {
      width: 290px;
      padding-top: 50px;
    }
  }
}
@include media(md) {
  .hero {
    height: calc(50vh - 78px);
    padding-top: 0px;
  }
  .social {
    .img {
      width: 400px;
    }
    .social_links {
      justify-content: flex-start !important;
    }
  }
}

</style>