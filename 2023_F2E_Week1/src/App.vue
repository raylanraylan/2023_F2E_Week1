<script setup>

</script>
<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import { defineComponent,ref,onMounted } from 'vue';

export default defineComponent( {
  components: {
    Splide,
    SplideSlide,
  },

  setup() {
    const options = {
      type   : 'loop',
      padding: '3rem',
      gap: '20px',
      drag: true,
      arrows: false,
      updateOnMove: true,
    };

    return { options };
  },
  },
);
// Default theme
// import '@splidejs/vue-splide/css';

// or other themes
import '@splidejs/vue-splide/css/skyblue';
// import '@splidejs/vue-splide/css/sea-green';
import './assets/splide.css';
// or only core styles
// import '@splidejs/vue-splide/css/core';
</script>

<template>
  <header class="header" id="index">
    <nav class="navbar bg-body-tertiary fixed-top">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="./assets/img/name_blue.png" alt="候選人號碼" class="candidate_name">
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar" aria-label="Toggle navigation">
          <img src="./assets/img/menu (1) 1.png">
        </button>
        <div class="offcanvas offcanvas-end" ref="offcanvas" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <h1 class="offcanvas-title" id="offcanvasNavbarLabel">
              <img src="./assets/img/name_white.png">
            </h1>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
              <img src="./assets/img/close 1.png" class="close_img">
            </button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1">
              <li class="nav-item">
                <h5><a class="nav-link active" aria-current="page" href="#cover" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">候選人主張</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#news" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">最新活動</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#policy" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">政策議題</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#public_feedback" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">民眾服務信箱</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#donation" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar"><img src="./assets/img/donate.png"></a></h5>
              </li>
            </ul>
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
            <div class="cover_text" id="cover">
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
    <section class="news" id="news">
      <h3>
        <img src="./assets/img/news.png" alt="最新消息">
      </h3>
      <Splide :options="options" aria-label="news content">
        <SplideSlide>
          <div class="card">
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
        </SplideSlide>
        <SplideSlide>
          <div class="card">
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
        </SplideSlide>
        <SplideSlide>
          <div class="card">
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
        </SplideSlide>
      </Splide>

    </section>
    <section class="policy" id="policy">
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
    <section class="donation" id="donation">
      <div class="donation_container">
        <div class="donation_description">
          <div class="donation_title_text_img">
            <img src="./assets/img/small donation.png" alt="小額捐款">
          </div>
          <p class="donation_text">您的小筆捐款，
            是每隻毛孩未來的大大動力！</p>
          <div class="donation_totalAmount">
            <div class="donation_totalAmount_text_img">
              <img src="./assets/img/total amount.png" alt="累積總金額">
            </div>
            <span class="total_amount">NT$<span class="number">987,655,873</span></span>
          </div>
          <button type="button" class="donation_button">
            <img src="./assets/img/Btn.png" alt="前往捐款的按鈕">
          </button>
        </div>
        <form class="donation_content">
          <h4 class="donation_plan_title">選擇捐款方案</h4>
          <div class="donation_plan">
            <div class="plan">
              <h6>喵星人之友</h6>
              <span class="amount">NT$600</span>
              <span class="sponsors_number">已有 9957 人贊助</span>
            </div>
            <div class="plan">
              <h6>喵星人之友</h6>
              <span class="amount">NT$600</span>
              <span class="sponsors_number">已有 9957 人贊助</span>
            </div>
            <div class="plan">
              <h6>喵星人之友</h6>
              <span class="amount">NT$600</span>
              <span class="sponsors_number">已有 9957 人贊助</span>
            </div>
            <div class="plan">
              <h6>自訂捐款金額</h6>
              <input class="input_amount" type="text" placeholder="請輸入捐款金額">
            </div>
          </div>
          <div class="button_container">
            <button class="back"><img src="./assets/img/Property 1=Back, Size=Small.png"></button>
            <button class="submit" type="button" data-bs-toggle="modal" data-bs-target="#donationSubmit"><img src="./assets/img/Property 1=Default, Size=Small.png"></button>
            <div class="modal fade" id="donationSubmit" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
              <div class="modal-dialog">
                <div class="modal-content">
                  <div class="modal-header">
                    <h4 class="modal-title fs-5" id="staticBackdropLabel">感謝您成為喵星大使</h4>
                  </div>
                  <div class="modal-body">
                    <div class="amount_text">
                      <img src="./assets/img/donation.png">
                    </div>
                    <span class="amount">NT$<span>6,000</span></span>
                  </div>
                  <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal" data-bs-target="#staticBackdrop">
                      <img src="./assets/img/Property 1=Back, Size=Small.png" alt="返回按鍵">
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </form>
      </div>  
    </section>
    <section class="public_feedback" id="public_feedback">
      <form class="public_feedback_container">
        <h3 class="public_feedback_title_text_img"><img src="./assets/img/feedback.png"></h3>
        <h5 class="public_feedback_slogan">您的聲音，我們的行動！</h5>
        <p class="public_feedback_text">親愛的鄉親，每一位市民的意見都是我們社區前進的原動力。無論大小事，我都誠摯希望聽到您的建議。分享您的想法，一同為我們的未來打造更美好！</p>
        <div class="form_content">
          <div class="form-floating">
            <input type="text" class="form-control" id="nameInput" placeholder="">
            <label for="nameInput">您的姓名</label>
          </div>
          <div class="form-floating">
            <input type="email" class="form-control" id="emailInput" placeholder="">
            <label for="emailInput">您的Email</label>
          </div>
          <div class="form-floating">
            <input type="text" class="form-control" id="phoneInput" placeholder="">
            <label for="phoneInput">您的手機</label>
          </div>
          <div class="form-floating">
            <textarea class="form-control" id="messageInput" placeholder=""></textarea>
            <label for="messageInput">您的建言</label>
          </div>
        </div>  
        <button type="button" class="btn btn-primary public_feedback_submit" data-bs-toggle="modal" data-bs-target="#feedbackSubmit">
          <img src="./assets/img/submit.png" alt="送出意見的按鍵">
        </button>
        <div class="modal fade modal_set" id="feedbackSubmit" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title fs-5" id="staticBackdropLabel">感謝您抽出寶貴的時間給予我們寶貴的建議。</h5>
              </div>
              <div class="modal-body">
                <p>我們非常重視您的意見，它是我們不斷改進和提升服務的動力。您提出的建議已經轉交給相關部門進行評估，我們將努力在未來的服務中加以考慮和實施。</p>
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">
                  <img src="./assets/img/Property 1=Back, Size=Small.png" alt="返回按鍵">
                </button>
              </div>
            </div>
          </div>
        </div>
      </form>
    </section>
    <div class="cat_img">
      <img src="./assets/img/Mokker (6) 1.png" alt="貓咪照片"> 
    </div>
  </main>

  <footer>
    <div class="menu">
      <span class="menu_title">Menu</span>
      <div class="menu_link">
        <a href="#index" class="menu_link_item">首頁</a>
        <a href="#news" class="menu_link_item">最新活動</a>
        <a href="#public_feedback" class="menu_link_item">民眾服務信箱</a>
        <a href="#cover" class="menu_link_item">候選人主張</a>
        <a href="#policy" class="menu_link_item">政策議題</a>
        <a href="#donation" class="menu_link_item">小額捐款</a>
      </div>
    </div>
    <div class="office_information">
      <span class="office_information_title">Office information</span>
      <address>
        <span class="address">地址：<a href="https://www.google.com.tw/maps/place/台北市喵星區毛茸茸大道88號喵喵大樓3樓">台北市喵星區毛茸茸大道88號喵喵大樓3樓</a></span>
        <span class="phone">電話：<a href="tel:(02)888-5678">(02)888-5678</a></span>
        <span class="mail">郵件：<a href="mailto:meowoffice@linmeow.tw">meowoffice@linmeow.tw</a></span>
      </address>
    </div>
    <span class="copyright">版權聲明：&copy; 2023 喵立翰（Miao Li-Han） 版權所有。</span>
  </footer>
</template>

<style lang="scss" scoped>

//nav
.header{
  nav{
    margin: 0 5px 0;
    padding:14px 17px 14px 20px;
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
    margin-bottom: 27px;
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
    box-shadow: none;
  }

  .offcanvas-body{
    padding: 0;
    
    .navbar-nav{
      display: flex;
      gap:30px;
    }

    h5{
      margin-bottom: 0;
    }

    a{
      padding: 0;
      color:$white;
    }
  }
}

main{
  margin: 65px 5px 0;
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

.cover_container{
  position: relative;
  padding: 20px 0 35px;
  margin: 0 15px;
}

.election_text_img{
  text-align: center;
} 

h3{
  margin-bottom: 25px;
  text-align: center;
  color:$dark1;
}

.news{
  padding: 0 0 30px;

  .splide__slide>.card{
    &::after{
      content:"";
      position:absolute;
      width:100%;
      height:100%;
      background-color:rgba(255,255,255,.5);
    }
    .card-img{
      height:188px;
    }

    .card-body{
      height:168px;
    }

  }
  .is-active>.card {
    &::after{
      background-color:rgba(255,255,255,0);
    }

    .card-img{
      height:200px;
    }
  }

  .splide__slide img{
    height: 200px;
    object-fit:cover;
  }

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

    &-title{
      margin-bottom: 10px;
      color:$dark1;
    }

    &-body{
      text-align: left;
      padding: 15px;
      position: relative;

      &::after{
        content: "";
        position: absolute;
        width: 27.528px;
        height: 15.64px;
        top:-15.64px;
        left:46%;
        clip-path: polygon(50% 0 ,100% 100%,0 100%);
        background-color: $white;
      }
    }

    &-text{
      font-size: $font-normal;
      display: -webkit-box;
      overflow: hidden;
      -webkit-box-orient: vertical;
      -webkit-line-clamp: 3;
      color:$dark2;
    }
  }
}

.policy{
  padding: 20px 0 50px;

  article{
    display:flex;
    flex-direction: column;
    align-items: center;
    gap:20px;
  }

  .card{
    width: 330px;
    padding:15px;
    border-radius: 8px;
    background-color: $light5;

    letter-spacing:-0.4px;
    &_content-number{
      width: 68px;
      height: 34px;
      padding: 5px 10px;
      margin-bottom: 10px;
      border-radius: 8px 0;
      background-color: $secondary_green;
      font-size: $font_medium;
      color:$light5;
    }
    &-body{
      padding:0;
    }

    &-title{
      margin-bottom: 10px;
      color:$dark1;
    }

    &-text{
      padding-left: 15px;
      color: $dark2;
    }
  }
}

.donation{
  padding:45px 16.5px;
  background: no-repeat center/cover url('./assets/img/female-hand-with-cat-paw-kitten-s-paw-woman-finger-contrast-close-up 1.png');

  &_container{
    padding: 62px 30px;
    background-color: $light5;
    border-radius: 80px;
    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.10);
    text-align: center;
  }

  .donation_description {
    display: flex;
    flex-direction: column;
    gap:20px;

    .donation_text{
      word-break: keep-all;
    }

    .total_amount{
      font-size: 30px;
      font-weight: 700;
      -webkit-text-stroke:2px $main_blue;
      color:$main_blue;
    }

    .donation_button{
      border: none;
      background-color:$light5;
    }
  }
  
  .donation_content{
    display: none;
  }

  h4{
    margin-bottom:10px;
  }
  .donation_plan{
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr;
    gap:10px;
    margin-bottom:10px;
  
    .plan{
      display: flex;
      flex-direction: column;
      gap:5px;
      padding: 15px 3px;
      border:solid 2px $light1;
      border-radius:8px;
      background-color: $white;
    }

    h6{
      margin-bottom: 0;
    }
    .amount{
      font-size: $title_s;
      font-weight: 700;
      -webkit-text-stroke:2px $main_blue;
      color:$main_blue;
    }

    .sponsors_number{
      font-size: $font_small;
      color:$dark5;
    }

    input{
      align-self: center;
      padding:12px 6px;
      border: 1px solid $light2;
      border-radius: 8px;
      width:120px;
      height: 50px;
      
      font-size: $font_normal;
      text-align: center;
      color:#C1C1C1;
    }
  }

  .button_container{
    display:flex;
    gap: 10px;

    button{
      border:0;
      background-color: $light5;
    }
    
    .back>img,.submit>img{
      margin:0 auto;
      display:block;
      width:93%;
    }
    .modal{
      .modal-content{
        display: flex;
        padding:60px 67px;
        border-radius: 80px;
      }
      .modal-header{
        padding: 0;
        margin-bottom: 10px;
        border:0;

        h4{
          width:100%;
          text-align:center;
        }
      }

      .modal-body{
        display: flex;
        flex-direction: column;
        padding: 0;
        margin-bottom: 50px;

        .amount{
          font-size: 30px;
          font-weight: 700;
          -webkit-text-stroke:2px $main_blue;
          color:$main_blue;
        }
      }
      .modal-footer{
        display: block;
        padding: 0;
        border:0;

        button{
          background-color: $white;
        }
      }

    }
  }
}

.public_feedback_container{
  padding: 20px 15px 130px;
  text-align: center;
  .public_feedback_text{
    margin-bottom: 15px;
    font-size: $font_normal;
  }

  .form_content{
    display: flex;
    flex-direction: column;
    gap:10px;
  }

  form-control,label{
    padding: 10px;
    font-size: $font_normal;
    color:#C1C1C1;
  }

  input,textarea{
    border: 1px solid $light2;
  }

  input:focus{
    box-shadow: none;
  }

  textarea.form-control{
    height: 80px;
  }

  .public_feedback_submit{
    border: none;
    background-color: #E3E3E3;

    &:active{
      background-color: #E3E3E3;
    }
  }

  .modal_set{
    text-align: center;
    .modal-content{
      display: flex;
      padding:30px;
      border-radius: 80px;
    }
    .modal-header{
      padding: 0;
      margin-bottom: 10px;
      border:0;

      h5{
        width:100%;
        text-align:center;
      }
    }

    .modal-body{
      padding: 0;
      margin-bottom: 50px;
    }
    .modal-footer{
      display: block;
      padding: 0;
      border:0;
    }

    .btn-secondary{
      margin: 0;
      padding:0;
      border: none;
      background-color: $white;
      text-align: center;
    }
  }
}

.cat_img{
  position: absolute;
  // top: -120.864px;
  top:3660px;
  // top:3652px;
  left: 18px;

  img{
    width: 355px;
  }
}

footer{
  padding:30px 21px 15px;
}
.menu{
  margin-bottom: 60px;
  text-align: center;

  &_title{
    display:block;
    margin-bottom: 10px;
    font-size: $font_small;
    color:$secondary_orange;
  }

  &_link{
    columns: 2;

    a{
      display: block;
      margin-bottom: 5px;
      font-size: $font_normal;
      color:$light5;

      &:nth-child(3n){
        margin-bottom: 0px;
      }
    }
  }
}

.office_information{
  margin-bottom: 20px;
  &_title{
    display:block;
    margin-bottom: 10px;
    text-align: center;
    font-size: $font_small;
    color:$secondary_orange;
  }

  address{
    display:flex;
    flex-direction: column;
    gap:5px;

    span{
      display:block;
      color:$light5;
    }

    .mail a{
      text-decoration:underline;
    }
  }
}

.copyright{
  display:block;
  text-align: center;
  font-size: $font_small;
  color:$dark5;
}

</style>
