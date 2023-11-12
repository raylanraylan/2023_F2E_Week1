<script setup>

  // document.querySelector('.swiper-pagination').style.position = ''
</script>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';

  // import './style.css';

  // import required modules
  import { Pagination } from 'swiper/modules';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination],
      };
    },
  };
</script>

<template>
  <header>
    <nav class="navbar bg-body-tertiary fixed-top">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Offcanvas navbar</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <h1 class="offcanvas-title" id="offcanvasNavbarLabel">Offcanvas</h1>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Link</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  Dropdown
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" href="#">Action</a></li>
                  <li><a class="dropdown-item" href="#">Another action</a></li>
                  <li>
                    <hr class="dropdown-divider">
                  </li>
                  <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
              </li>
            </ul>
            <form class="d-flex mt-3" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
          </div>
        </div>
      </div>
    </nav>
  </header>

  <main>
    <section class="cover">
      <div class="cover_container">
        <h2 class="cover_slogan">
          <div class="election_text_img">
            <img src="./assets/img/2023_THE_F2E_legislative election.png" alt="宣傳標語：2023 the f2e 立委競選">
          </div>
          <div class="cat_eye_text_img">
            <img src="./assets/img/Seeing Taiwan through the eyes of cats.png" alt="宣傳標語：從喵的眼中看見台灣">
          </div>
        </h2>
        <div class="candidate">
            <img src="./assets/img/candidate.png" alt="候選人照片">
          </div>
        <div class="cover_content">
          <div class="keep_it_possible">
            <img src="./assets/img/KEEP IT POSSIBLE.png" alt="宣傳標語：keep it possible">
          </div>
          <div>
            <div class="miao_Li-Han_text_img">
              <img src="./assets/img/Miao Li-Han.png">
            </div>
            <div class="cover_text">
              <h5>
                護航台灣幸福經濟  
                從照顧每一隻貓咪開始
              </h5>
              <p>我堅信，藉由推動更完善的貓咪福利和相關政策，更是間接地投資於台灣的未來。畢竟，民眾的身心健康與工作熱情是推動經濟的核心動力。透過完善的貓咪福利政策，為台灣的 GDP 經濟帶來巨大效益。</p>
              <p>因此，我期望能在立法院內推進這些政策，確保每一隻貓咪都能得到他們應有的照顧，同時也為台灣的經濟發展助一臂之力。</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="news">
      <h3>
        <img src="./assets/img/news.png" alt="最新消息">
      </h3>
      <swiper
      :slidesPerView="'auto'"
      :centeredSlides="true"
      :loop="true"
      :spaceBetween="10"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      class="mySwiper">
        <swiper-slide>
          <div class="card" style="width: 20rem;">
            <time class="card_date">
              <span class="day">26</span>
              <span class="month">DEC.</span>
            </time>
            <div class="card-img">
              <img src="./assets/img/activity01.png" class="card-img-top" alt="">
            </div>
            <div class="card-body">
              <h5 class="card-title">參與台北寵物論壇 爭取貓咪友善環境</h5>
              <p class="card-text">炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中，每一隻貓咪都應該有自己的 VIP 休憩空間。</p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card" style="width: 20rem;">
            <time class="card_date">
              <span class="day">26</span>
              <span class="month">DEC.</span>
            </time>
            <div class="card-img">
              <img src="./assets/img/activity01.png" class="card-img-top" alt="">
            </div>
            <div class="card-body">
              <h5 class="card-title">參與台北寵物論壇 爭取貓咪友善環境</h5>
              <p class="card-text">炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中，每一隻貓咪都應該有自己的 VIP 休憩空間。</p>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="card" style="width: 20rem;">
            <time class="card_date">
              <span class="day">26</span>
              <span class="month">DEC.</span>
            </time>
            <div class="card-img">
              <img src="./assets/img/activity01.png" class="card-img-top" alt="">
            </div>
            <div class="card-body">
              <h5 class="card-title">參與台北寵物論壇 爭取貓咪友善環境</h5>
              <p class="card-text">炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中，每一隻貓咪都應該有自己的 VIP 休憩空間。</p>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </section>
    <section class="policy">
      <h3>
        <img src="./assets/img/policy.png" alt="政策議題">
      </h3>
      <article class="policy_content">
        <div class="card">
          <div class="card_content-number">政策一</div>
          <div class="card-body">
            <h5 class="card-title">
              為毛孩子謀福利！推動寵物醫療保障方案
            </h5>
            <ol class="card-text">
              <li>設立寵物醫療基金：每年撥款新台幣 10 億元，專款專用於支援家庭寵物的醫療費用</li>
              <li>提供醫療補助：每隻寵物每年可獲得高達新台幣 20,000 元的醫療補助，減輕飼主的經濟壓力</li>
              <li>合作動物醫院：目前已有和超過 200 家動物醫院進行初步的合作討論</li>
            </ol>
          </div>
        </div>
        <div class="card">
          <div class="card_content-number">政策二</div>
          <div class="card-body">
            <h5 class="card-title">
              打造休閒天堂！推廣寵物休閒與娛樂場所
            </h5>
            <ol class="card-text">
              <li>建立寵物公園：每年撥款新台幣 5 億元，用於在各大都市建立專屬的寵物公園。</li>
              <li>推廣寵物友善商家：鼓勵商家提供寵物友善的環境，並為參與的商家提供稅收優惠。預計在政策實施後的首年，將有超過 500 家商家加入此計畫</li>
              <li>舉辦寵物活動和工作坊：與各大寵物社團和組織合作，每年舉辦至少 5 場大型的寵物活動，包括寵物才藝比賽、飼養知識工作坊等</li>
            </ol>
          </div>
        </div>
        <div class="card">
          <div class="card_content-number">政策三</div>
          <div class="card-body">
            <h5 class="card-title">
              推廣寵物飼養教育，讓愛更加專業
            </h5>
            <ol class="card-text">
              <li>建立寵物飼養教育中心：每年撥款新台幣 3 億元，用於在全國各地建立專業的寵物飼養教育中心。預計在第一年內，在全國至少 5 大城市設立教育中心。</li>
              <li>推廣寵物飼養課程：與學校、社區組織和寵物社團合作，推出一系列免費的寵物飼養課程。預計每年將有超過 10,000 名市民受益。</li>
              <li>製作教育資料：出版寵物飼養手冊、影片和線上課程，讓所有有意飼養寵物的家庭都能輕鬆取得正確的知識</li>
            </ol>
          </div>
        </div>
      </article>
    </section>
    <section class="donate"></section>
    <section class="public_feedback">
      <div class="public_feedback_container"></div>
    </section>
  </main>

  <footer>

  </footer>
</template>

<style lang="scss" scoped>  
@import "@/scss/swiper.scss";
//nav
nav{
  margin: 0 5px 0;
}
.offcanvas{
  transition:none;
}

main{
  margin: 55px 5px 0;
}
.cover,.news,.public_feedback{
  background-color: #E3E3E3;
}

//cover
.cover{

  &_slogan{
    margin-bottom: 20px;
  }

  &_content{
    display: flex;
    .keep_it_possible{
      margin-left: -5px;
      margin-right: 10px;
    }

    .miao_Li-Han_text_img{
      margin-bottom: 70px;
    }
  }

  &_text{
    padding: 10px;
    position: relative;
    background-color: white;
    border: 3px solid $main_blue;
    border-radius: 80px 0;
    box-shadow: -5px 5px 0px $main_blue;
  }

  &_text>h5{
    margin-bottom: 10px;
    text-align: center;
    word-break: keep-all;
  }

  &_text>p{
    font-size: $font_normal;
    font-weight: 500;

    &:first-of-type{
      margin-bottom: 20px;
    }
  }
}

.candidate{
  position: absolute;
  top: 16%;
  left: 32%;

  img{
    width: 102%;
  }
}

.cover_container,.public_feedback{
  margin: 40px 15px 0px;
}

.cover_container{
  position: relative;
  padding: 20px 0 20px;
}

.election_text_img{
  text-align: center;
} 



h3{
  text-align: center;
  margin-bottom: 30px;
}

.news{
  padding: 20px 0 50px;
.card{
  position: relative;
  border-radius: 8px;
  &_date{
    position: absolute;
    top: 0;
    right: 0;
    width: 65px;
    height: 65px;

    display: flex;
    flex-direction: column;
    align-items: center;

    background-color: $secondary_green;
    border-radius: 0 8px 0 0;
    .day,.month{
      font-weight: 700;
      color:white;
    }
    .day{
      font-size: 30px;
    }
    .month{
      font-size: $font_normal;
      line-height: 20px; 
    }
  }

  &-img{
    height: 200px;
  }

  &-body{
    text-align: left;
    padding: 15px;
  }

  &-title{
    margin-bottom: 10px;
  }

  &-text{
    font-size: $font-normal;
    display: -webkit-box;
    overflow: hidden;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
  }
}
}

.policy{
  padding: 20px 31.5px 50px;

  article{
    display:flex;
    flex-direction: column;
    gap:20px;
  }

  .card{
    padding:15px;
    border-radius: 8px;
    background-color: $light5;
    &_content-number{
      width: 68px;
      height: 34px;
      padding: 5px 10px;
      margin-bottom: 10px;
      border-radius: 0 8px;
      background-color: $secondary_green;
      font-size: $font_medium;
      color:$light5;
    }
    &-body{
      padding:0;
    }
  }
}

</style>
