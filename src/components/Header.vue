<script setup>
import { ref } from 'vue';

const activeLink = ref(null);
const offcanvas = ref(null);

const addUnderline = (event)=>{
  // closeOffcanvas();
  if (window.innerWidth<1512) return;
  activeLink.value = event.target.dataset.name;
}
</script>
<template>
  <header class="header" id="index">
    <nav class="navbar bg-body-tertiary fixed-top navbar-expand-xxl">
      <div class="container-fluid">
        <a class="navbar-brand" href="#index">
          <img class="candidate_name" src="../assets/img/Logo (2).png" alt="候選人名字">
        </a>
        <button class="navbar-toggler" type="button" aria-controls="offcanvasNavbar" aria-label="Toggle navigation"  data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">
          <img src="../assets/img/menu (1) 1.png" alt="連結選單按鍵">
        </button>
        <div class="offcanvas offcanvas-end" ref="offcanvas" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <h1 class="offcanvas-title" id="offcanvasNavbarLabel">
              <img src="../assets/img/name_white.png" alt="候選人名字">
            </h1>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
              <img class="close_img" src="../assets/img/close 1.png" alt="關閉連結選單">
            </button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1">
              <li class="nav-item">
                <h5>
                  <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
                    <a class="nav-link" data-name="cover" :class="{active:activeLink==='cover'}" aria-current="page" href="#cover" @click="addUnderline">候選人主張</a>
                  </button>
                </h5>
              </li>
              <li class="nav-item">
                <h5>
                  <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
                    <a class="nav-link" data-name="news" :class="{active:activeLink==='news'}" href="#news" @click="addUnderline">最新活動</a>
                  </button>
                </h5>
              </li>
              <li class="nav-item">
                <h5>
                  <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
                    <a class="nav-link" data-name="policy" :class="{active:activeLink==='policy'}" href="#policy" @click="addUnderline">政策議題</a>
                  </button>
                </h5>
              </li>
              <li class="nav-item">
                <h5>
                  <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
                    <a class="nav-link" data-name="public_feedback" :class="{active:activeLink==='public_feedback'}" href="#public_feedback" @click="addUnderline">民眾服務信箱</a>
                  </button>
                </h5>
              </li>
              <li class="nav-item nav-item-phone">
                <h5><a class="nav-link" href="#donation" @click="addUnderline"></a></h5>
              </li>
              <li class="nav-item nav-item-pc">
                <h5>
                  <a class="nav-link" href="#donation"></a>
                </h5>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>
<style lang="scss">

.header{
  nav{
    margin: 0 5px;
    padding:14px 17px 14px 20px;
    border-top: 5px solid  #4527A0; 
    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.25);
  
    @include breakpoint($PC){
      padding: 18px 151px;
    }
  }
  .container-fluid{
    padding:0;
  }
  .offcanvas{
    padding: 17px 20px;
    transition:none;
    background-color: $main_blue;
    text-align: right;
    color:$white;
  }
  .offcanvas-header{
    padding: 0;
    margin-bottom: 25px;
  }
  .candidate_name{
    width:150px;
    @include breakpoint($PC){
      width: auto;
    }
  }

  h1{
    line-height: 0;
  }

  .btn-close{
    align-self: center;
    width: 30px;
    height: 30px;
    padding:0px;
    margin:0px;
    background:none;
    opacity: 1;
  }

  .navbar-brand{
    display: flex;
    align-items: center;
    gap:3px;
  }

  .navbar-toggler{
    padding:0;
    border: none;
    
    &:focus{
      box-shadow: none;
    }
  }

  .offcanvas-body{
    padding: 0;
    
    .navbar-nav{
      display: flex;
      @include breakpoint($PC){
        align-items: center;
        gap:50px;
      }
    }

    .nav-item{
      .btn-close{
        --bs-btn-close-bg:none;
        padding: 0;
        width: auto;
        height: auto;
        font-size: 20px;
      }

      // &:nth-child(4){
      //   margin-bottom: 15px;
      // }
    }

    .nav-item-phone{
      margin-left: auto;
      @include breakpoint($PC){
        display:none;
      }

      h5{
        width:fit-content;
      }

      a{
        width:160px;
        height:52px;
        background:no-repeat url('../assets/img/donate.png');
        
        &:hover{
          background:no-repeat url('../assets/img/Property 1=Default, Size=Small.png');
        }
      }
    }

    .nav-item-pc{
      display:none;
      @include breakpoint($PC){
        display: block;
      }

      h5{
        width:fit-content;
      }

      a{
        width:160px;
        height:52px;
        background:no-repeat url('../assets/img/Property 1=Default, Size=Small.png');
        
        &:hover{
          background:no-repeat url('../assets/img/donate.png');
        }
      }
    }

    h5{
      margin-bottom: 0;
    }

    a.nav-link{
      color:$white;
      padding: 15px 0;
      @include breakpoint($PC){
        color:black;
      }
    }

    a.active{ 
      border-bottom:3px solid $main_blue;
    }
  }
}
</style>