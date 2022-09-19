<template>
 <div class="container py-2" id="nav">
    <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container-fluid d-flex justify-content-between align-items-center">
            <a class="navbar-brand" href="#"><img src="../assets/logo/logo.svg" alt=""></a>
            <fa icon="list" width="25px" class="text-white fs-1 nav_shower" @click="ShowNav"/>
            <div class="collapse navbar-collapse" id="navbarSupportedContent" :class ="{show:state.status}">
                    <ul
                    class="navbar-nav me-auto mb-2 mb-lg-0 d-flex align-items-sm-start align-items-lg-center w-100 justify-content-end">
                    <li class="nav-item mx-lg-3">
                        <a class="nav-link  active text-white" aria-current="page" href="#">Home</a>
                    </li>
                    <li class="nav-item  mx-lg-3">
                        <a class="nav-link  active text-white" href="#sec-3">About</a>
                    </li>
                    <li class="nav-item  mx-lg-3">
                        <a class="nav-link  active text-white" href="#sec-4" tabindex="-1"
                                        aria-disabled="true">Project</a>
                    </li>
                    <li class="nav-item  mx-lg-3">
                        <a class="nav-link  active text-white" href="#sec-5" tabindex="-1"
                                        aria-disabled="true">Blog</a>
                    </li>
                    <li class="nav-item  mx-lg-3">
                        <a class="py-2 w-100 btn bg-outline-main-color  active text-main-color">Contact
                                        Me</a>
                    </li>
                </ul>
            </div>
        </div>
        </nav>
 </div>
</template>

<script>
import { reactive } from 'vue'
export default {
    name: 'HeaderApp',
    setup() {

        const state = reactive({
            status:false
        })

        function ShowNav() {
            state.status = !state.status;
        } 
        return {
            state,
            ShowNav
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../sass/main';
    nav {
  .container-fluid {
    .collapse {
      ul {
        li {
          a {
            font-weight: 550;
            &:hover {
              color: $main-color !important;
            }
          }
        }
        :last-child {
          a {
            &:hover {
              background-color: $main-color;
              color: $white-color-1 !important;
            }
          }
        }
      }
    }
  }
}
nav {
  .container-fluid {
    .show {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background-color: $main-color-dark_2;
      animation: hider_scaler 1s ease-in-out;
      ul {
        li {
          width: 95%;
          margin: 0 auto;
          a {
            color: $main-color !important;
            background-color: transparent;
            border: 2px solid $main-color;
            padding: 10px 0;
            margin: 10px 0;
            animation: hider_scaler 1s ease-in-out;
            animation-delay: 0.1s;
            text-align: center;
            &:hover {
              background-color: $main-color;
              color: $white-color-1 !important;
            }
          }
        }
      }
    }
  }
}
.active-nav {
  background-color: $main-color-dark_2 !important;
  position: fixed;
  top: -20%;
  z-index: 1000;
  width: 100%;
  padding: 0 30px;
  animation: nav 0.5s ease-in-out forwards;
}
@keyframes nav {
  from {
    top: -20%;
  }
  to {
    top: 0%;
  }
}
@keyframes hider_scaler {
  from {
    transform: translateY(200px);
    opacity: 0;
  }

  to {
    transform: translateY(0px);
    opacity: 1;
  }
}
.nav_shower {
  cursor: pointer;
}
@include media(lg) {
  .nav_shower {
    display: none;
  }
}

</style>