<script setup>

</script>
<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import { defineComponent } from 'vue';

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

import '@splidejs/vue-splide/css/skyblue';
import './assets/splide.css';
</script>

<template>
  <header class="header" id="index">
    <nav class="navbar bg-body-tertiary fixed-top navbar-expand-xxl">
      <div class="container-fluid">
        <a class="navbar-brand" href="#index">
          <img class="candidate_name" src="./assets/img/Logo (2).png" alt="候選人名字">
        </a>
        <button class="navbar-toggler" type="button" aria-controls="offcanvasNavbar" aria-label="Toggle navigation"  data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar">
          <img src="./assets/img/menu (1) 1.png" alt="連結選單按鍵">
        </button>
        <div class="offcanvas offcanvas-end" ref="offcanvas" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
          <div class="offcanvas-header">
            <h1 class="offcanvas-title" id="offcanvasNavbarLabel">
              <img src="./assets/img/name_white.png" alt="候選人名字">
            </h1>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close">
              <img class="close_img" src="./assets/img/close 1.png" alt="關閉連結選單">
            </button>
          </div>
          <div class="offcanvas-body">
            <ul class="navbar-nav justify-content-end flex-grow-1">
              <li class="nav-item">
                <h5><a class="nav-link active" aria-current="page" href="#cover">候選人主張</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#news">最新活動</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#policy">政策議題</a></h5>
              </li>
              <li class="nav-item">
                <h5><a class="nav-link" href="#public_feedback">民眾服務信箱</a></h5>
              </li>
              <li class="nav-item nav-item-phone">
                <h5><a class="nav-link" href="#donation"></a></h5>
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

  <main>
    <section class="cover">
      <div class="cover_container">
        <h2 class="cover_slogan_phone">
          <div class="election_text_img">
            <img src="./assets/img/2023_THE_F2E_legislative election.png" alt="宣傳標語：2023 the f2e 立委競選">
          </div>
          <div class="cat_eye_text_img">
            <img src="./assets/img/Seeing Taiwan through the eyes of cats.png" alt="宣傳標語：從喵的眼中看見台灣">
          </div>
        </h2>
        <h2 class="cover_slogan_pc">
          <div class="election_text_img">
            <img src="./assets/img/2023_THE_F2E_legislative election_PC.png" alt="宣傳標語：2023 the f2e 立委競選">
          </div>
          <div class="cat_eye_text_img">
            <img src="./assets/img/Seeing Taiwan through the eyes of cats_PC.png" alt="宣傳標語：從喵的眼中看見台灣">
          </div>
        </h2>
        <div class="candidate">
            <img src="./assets/img/candidate.png" alt="候選人照片">
          </div>
        <div class="cover_content">
          <div class="keep_it_possible_phone">
            <img src="./assets/img/KEEP IT POSSIBLE.png" alt="宣傳標語：keep it possible">
          </div>
          <div class="keep_it_possible_pc">
            <img src="./assets/img/Frame 1.png" alt="宣傳標語：keep it possible">
          </div>
          <div class="cover_text_pc" id="cover">
            <h5>
              護航台灣幸福經濟  
              從照顧每一隻貓咪開始
            </h5>
            <p>我堅信，藉由推動更完善的貓咪福利和相關政策，更是間接地投資於台灣的未來。畢竟，民眾的身心健康與工作熱情是推動經濟的核心動力。透過完善的貓咪福利政策，為台灣的 GDP 經濟帶來巨大效益。</p>
            <p>因此，我期望能在立法院內推進這些政策，確保每一隻貓咪都能得到他們應有的照顧，同時也為台灣的經濟發展助一臂之力。</p>
          </div>
          <div>
            <div class="miao_Li-Han_text_img_phone">
              <img src="./assets/img/Miao Li-Han.png">
            </div>
            <div class="miao_Li-Han_text_img_pc">
              <img src="./assets/img/Miao Li-Han (1).png">
            </div>
            <div class="cover_text_phone" id="cover">
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
      <div class="news_title_text_img_phone">
        <img src="./assets/img/news.png" alt="最新消息">
      </div>
      <div class="news_title_text_img_pc">
        <img src="./assets/img/news_pc.png" alt="最新消息">
      </div>
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

      <div class="news_pc">
        <div class="card_latest_news">
          <div class="card">
            <time class="card_date">
              <span class="day">26</span>
              <span class="month">DEC.</span>
            </time>
            <div class="card-img">
              <img src="./assets/img/activity01.png" class="card-img-top" alt="活動照片">
            </div>
            <div class="card-body">
              <h5 class="card-title">參與台北寵物論壇 爭取貓咪友善環境</h5>
              <p class="card-text">炎炎夏日的周六，我走進了台北寵物論壇，帶著一副貓耳髮箍，決定要全力宣傳「貓咪至上」的理念！我相信，我們的都市中，每一隻貓咪都應該有自己的 VIP 休憩空間。</p>
            </div>
          </div>
        </div>
        <div class="card_old_news">
          <div class="card">
            <img src="./assets/img/activity01.png" class="card-img-top" alt="活動照片">
            <div class="card-body">
              <time class="card_date">
                <span class="date">2023.12.26</span>
              </time>
              <h5 class="card-title">Card title</h5>
              <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content.</p>
            </div>
          </div>
          <div class="card">
            <img src="./assets/img/activity01.png" class="card-img-top" alt="活動照片">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
            </div>
          </div>
        </div>  
      </div>
    </section>
    <section class="policy" id="policy">
      <div class="policy_title_text_img_small">
        <img src="./assets/img/policy.png" alt="政策議題">
      </div>
      <div class="policy_title_text_img_large">
        <img src="./assets/img/policy_large.png" alt="政策議題">
      </div>
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
          <div class="donation_title_text_img_small">
            <img src="./assets/img/small donation.png" alt="小額捐款">
          </div>
          <div class="donation_title_text_img_large">
            <img src="./assets/img/small donation_large.png" alt="小額捐款">
          </div>
          <p class="donation_text">您的小筆捐款，
            是每隻毛孩未來的大大動力！</p>
          <div class="donation_totalAmount">
            <div class="donation_totalAmount_text_img_small">
              <img src="./assets/img/total amount.png" alt="累積總金額">
            </div>
            <div class="donation_totalAmount_text_img_large">
              <img src="./assets/img/total amount_large.png" alt="累積總金額">
            </div>
            <span class="total_amount">NT$<span class="number">987,655,873</span></span>
          </div>
          <button type="button" class="donation_button_small">
            <img src="./assets/img/Btn.png" alt="前往捐款">
          </button>
          <button type="button" class="donation_button_large">
            <img src="./assets/img/Btn (1).png" alt="前往捐款">
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
            <button class="back"></button>
            <button class="submit" type="button" data-bs-toggle="modal" data-bs-target="#donationSubmit"></button>
          </div>
          <div class="modal fade" id="donationSubmit" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-header">
                  <h4 class="modal-title fs-5" id="staticBackdropLabel">感謝您成為喵星大使</h4>
                </div>
                <div class="modal-body">
                  <div class="amount_text">
                    <img src="./assets/img/donation.png" alt="捐款金額文字">
                  </div>
                  <span class="amount">NT$<span>6,000</span></span>
                </div>
                <div class="modal-footer">
                  <button type="button" class="btn btn-secondary" data-bs-dismiss="modal" data-bs-target="#staticBackdrop"></button>
                </div>
              </div>
            </div>
          </div>
        </form>
      </div>  
    </section>
    <section class="public_feedback" id="public_feedback">
      <form class="public_feedback_container">
        <div class="public_feedback_description">
          <div class="public_feedback_title_text_img_small"><img src="./assets/img/feedback.png"></div>
          <div class="public_feedback_title_text_img_large"><img src="./assets/img/feedback_large.png"></div>
          <h5 class="public_feedback_slogan">您的聲音，我們的行動！</h5>
          <p class="public_feedback_text">親愛的鄉親，每一位市民的意見都是我們社區前進的原動力。無論大小事，我都誠摯希望聽到您的建議。分享您的想法，一同為我們的未來打造更美好！</p>
        </div>
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
          <button type="button" class="btn btn-primary public_feedback_submit" data-bs-toggle="modal" data-bs-target="#feedbackSubmit">
            <img src="./assets/img/submit.png" alt="送出意見的按鍵">
          </button>
        </div>  
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
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal"></button>
              </div>
            </div>
          </div>
        </div>
      </form>
    </section>
  </main>
  
  <footer>
    <div class="cat_img">
      <img src="./assets/img/Mokker (6) 1.png" alt="貓咪照片"> 
    </div>
    <a href="#" class="candidate_name_text_img">
      <img class="candidate_name" src="./assets/img/Logo (1).png" alt="候選人名字">
    </a>
    <div class="menu">
      <span class="menu_title">Menu</span>
      <div class="menu_link">
        <div class="menu_link_container">
          <a href="#index" class="menu_link_item">首頁</a>
          <a href="#news" class="menu_link_item">最新活動</a>
          <a href="#public_feedback" class="menu_link_item">民眾服務信箱</a>
        </div>
        <div class="menu_link_container">
          <a href="#cover" class="menu_link_item">候選人主張</a>
          <a href="#policy" class="menu_link_item">政策議題</a>
          <a href="#donation" class="menu_link_item">小額捐款</a>
        </div>
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
    <span class="copyright">版權聲明：&copy;2023 喵立翰（Miao Li-Han） 版權所有。</span>
  </footer>
</template>

<style lang="scss" scoped>

//nav
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
    margin-bottom: 27px;
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
    box-shadow: none;
  }

  .offcanvas-body{
    padding: 0;
    
    .navbar-nav{
      display: flex;
      gap:30px;
      @include breakpoint($PC){
        align-items: center;
        gap:50px;
      }
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
        background:no-repeat url('./assets/img/donate.png');
        
        &:hover{
          background:no-repeat url('./assets/img/Property 1=Default, Size=Small.png');
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
        background:no-repeat url('./assets/img/Property 1=Default, Size=Small.png');
        
        &:hover{
          background:no-repeat url('./assets/img/donate.png');
        }
      }
    }

    h5{
      margin-bottom: 0;
    }

    a{
      padding: 0;
      font-size: 20px;
      color:$white;

      @include breakpoint($PC){
        padding-bottom: 10px;
        color:black;
      }
    }

    a.active{
      border-bottom:3px solid $main_blue
    }
  }
}

main{
  padding: 60px 0 0;

  @include breakpoint($PC){
    padding: 100px 0 0;
  }
}
.cover,.news,.public_feedback{
  background-color: #E3E3E3;
}

//cover
.cover{
  &_container{
    position: relative;
    padding: 30px 0 20px;
    margin: 0 15px;

    @include breakpoint($PC){
      display: flex;
      flex-direction: column;
      padding: 146px 0 50px;
      margin: 0 156px;
    }
  }

  &_slogan_phone{
    margin-bottom: 20px; 

    @include breakpoint($PC){
      display: none;
    }
    .election_text_img{
      text-align: center; 
    }
  }

  &_slogan_pc{
    display: none;

    @include breakpoint($PC){
      display: block;
    }

    .election_text_img{
      margin-bottom: 10px;
    }

    .cat_eye_text_img{
      margin-bottom: 18px;
    }
  }

  &_content{
    display: flex;
    .keep_it_possible_phone{
      margin-left: -5px;
      margin-right: 10px;

      @include breakpoint($PC){
        display: none;
      }
    }
    .keep_it_possible_pc{
      display: none;
      margin-left: -5px;
      margin-right: 10px;

      @include breakpoint($PC){
        display: block;
        margin-right: 60px;
      }
    }

    .miao_Li-Han_text_img_phone{
      margin-bottom: 70px;
      @include breakpoint($PC){
        display: none;
      }
    }

    .miao_Li-Han_text_img_pc{
      display: none;
      @include breakpoint($PC){
        display:block;
        position:absolute;
        left:53px;
      }
    }
  }

  &_text_phone{
    padding: 10px;
    position: relative;
    background-color: white;
    border: 3px solid $main_blue;
    border-radius: 80px 0;
    box-shadow: -5px 5px 0px $main_blue;
    @include breakpoint($PC){
      display: none;
    }

    h5{
      text-align: center;
      word-break: keep-all;
    }

    p{
      font-size: $font_normal;
      font-weight: 500;

      &:first-of-type{
        margin-bottom: 20px;
      }
    }
  }

  &_text_pc{
    display: none;
    @include breakpoint($PC){
      display: block;
      padding:40px 50px 50px 50px;
      margin-top:180px;
      position: relative;
      z-index:2;
      bottom: 20px;
      border: 5px solid $main_blue;
      border-radius: 80px 0;
      background-color: white;
      box-shadow: -10px 10px 0px $main_blue;
    }

    h5{
      text-align: center;
      margin-bottom: 33px;
      font-size: 44px;
      word-break:initial;
    }

    p{
      font-size: 24px;
      font-weight: 700;  

      &:first-of-type{
        margin-bottom: 20px;
      }
    }
  }
}

.candidate{
  position: absolute;
  top: 17%;
  left: 32%;

  @include breakpoint($PC){
    width: 42%;
    top:30px;
    left:628px;
    z-index:1;
  }

  img{
    width: 102%;

    @include breakpoint($PC){
      width: 100%;
    }
  }
}

.news{
  padding: 0 0 30px;

  @include breakpoint($PC){
    padding: 0 156px 45px;
  }
  
  .news_title_text_img_phone{
    margin-bottom: 25px;
    text-align: center;

    @include breakpoint($PC){
      display:none;
    }
  }

  .news_title_text_img_pc{
    margin-bottom: 25px;
    text-align: center;
    display:none;

    @include breakpoint($PC){
      display:block;
    }
  }
  .splide{
    @include breakpoint($PC){
      display:none;
    }
  }

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

  .news_pc{
    display: none;
    @include breakpoint($PC){
      display:flex;
      gap:30px;
    }
    .card_latest_news{
      .card{
        width:483px;
        padding-bottom: 20px;
      }

      .card_date{
        width: 75px;
        height: 75px; 
        font-size: $font_medium;
      }

      img{
        height:325px;
        object-fit:cover;
      }

      .day{
        font-size:36px;
        font-weight:700;
      }

      .card-title{
        font-size: 24px;
        font-weight: 700;
      }

      .card-text{
        font-size: $font_medium;
        font-style: normal;
        font-weight: 500;
      }
    }
    .card_old_news{
      display: flex;
      flex-direction: column;
      flex-grow: 1;
      gap:30px;
      padding:0;
      .card{
        flex-direction: row;
        width:auto;
      }

      img{
        width:276px;
        height:232px;
        object-fit:cover;
      }

      .card-body{
        &::after{
          display:none;
        }
      }
      .card_date{
        width: fit-content;
        height: auto;
        position:static;
        margin-bottom: 10px;
        padding:5px 10px;
        border-radius:8px 0px;
        font-size: $font_medium;
        color:$white;
      }
    }
  }
}

.policy{
  padding: 20px 20px 50px;

  @include breakpoint($PC){
    padding: 30px 156px 80px;
  }

  .policy_title_text_img_small{
    margin-bottom: 25px;
    text-align: center;

    @include breakpoint($PC){
      display: none;
    }
  }

  .policy_title_text_img_large{
    display: none;
    @include breakpoint($PC){
      display: block;
      margin-bottom: 30px;
      text-align: center;
    }
  }

  article{
    display:flex;
    flex-direction: column;
    align-items:center;
    gap:20px;

    @include breakpoint($PC){
      flex-direction: row;
      align-items:stretch;
      justify-content: center;
    }
  }

  .card{
    padding:15px;
    border-radius: 8px;
    background-color: $light5;
    @include breakpoint($PC){
      width: 379px;
    }
    &:nth-child(2){
      @include breakpoint($PC){
        position: relative;
        top:30px;
      }
    }
    
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
      display: -webkit-box;
      overflow: hidden;
      -webkit-box-orient: vertical;
      -webkit-line-clamp: 8;
      color: $dark2;
    }
  }
}

.donation{  
  display: flex;
  justify-content: center;
  align-items: center;
  padding:45px 20px;
  background: no-repeat center/cover url('./assets/img/female-hand-with-cat-paw-kitten-s-paw-woman-finger-contrast-close-up 1.png');
  @include breakpoint($PC){
    justify-content: left;
    padding:45px 156px;
  }

  &_container{
    width: 360px;
    // height: 398px;
    background-color: $light5;
    border-radius: 80px;
    box-shadow: 0px 0px 4px 0px rgba(0, 0, 0, 0.10);
    text-align: center;

    @include breakpoint($PC){
      width: 619px;
    }
  }

  .donation_description {
    display: flex;
    flex-direction: column;
    gap:20px;
    padding: 60px 30px;

    .donation_title_text_img_small{
      @include breakpoint($PC){
        display:none;
      }
    }

    .donation_title_text_img_large{
      display:none;
      @include breakpoint($PC){
        display:block;
      }
    }

    .donation_text{
      word-break: keep-all;

      @include breakpoint($PC){
        font-size: 24px;
      }
    }

    .donation_totalAmount_text_img_small{
      @include breakpoint($PC){
        display:none;
      }
    }

    .donation_totalAmount_text_img_large{
      display:none;
      @include breakpoint($PC){
        display:block;
      }
    }

    .total_amount{
      font-size: 30px;
      font-weight: 700;
      -webkit-text-stroke:2px $main_blue;
      color:$main_blue;

      @include breakpoint($PC){
        font-size:72px;
      }
    }

    .donation_button_small{
      border: none;
      background-color:$light5;
      @include breakpoint($PC){
        display:none;
      }
    }

    .donation_button_large{
      display:none;
      border:none;
      background-color:$light5;
      @include breakpoint($PC){
        display:block;
      }
    }
  }

  .donation_totalAmount_text_img_small{
    @include breakpoint($PC){
      display:none;
    }
  }

    .donation_totalAmount_text_img_large{
      display:none;
      @include breakpoint($PC){
        display:block;
      }
    }
  
  .donation_content{
    // display: none;
    padding: 20px 30px 30px;
    @include breakpoint($PC){
      padding:30px 60px;
    }
  }

  h4{
    margin-bottom:10px;
    @include breakpoint($PC){
      display:block;
      font-size:24px;
    }
  }

  .donation_plan{
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr;
    gap:10px;
    margin-bottom:10px;

    @include breakpoint($PC){
      display: flex;
      flex-wrap: wrap;
    }
  
    .plan{
      display: flex;
      flex-direction: column;
      // flex-grow: 1;
      gap:5px;
      padding: 15px 3px;
      border:solid 2px $light1;
      border-radius:8px;
      background-color: $white;
      @include breakpoint($PC){
        flex:1;
        padding: 15px 20px;
      }

      &:last-child{
        @include breakpoint($PC){
          flex-direction: row;
          justify-content: center;
          align-items: center;
          height:90px;
        }

        input{
          @include breakpoint($PC){
            padding: 14px 12px;
          }
        }
      }
    }

    h6{
      margin-bottom: 0;
      @include breakpoint($PC){
        font-size:20px;
        flex-grow: 40%;
      }
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
      &::placeholder{
        color:#C1C1C1;
      }

      @include breakpoint($PC){
        flex-grow: 1;
        font-size:$font-normal;
        text-align: left; 
      }
    }
  }

  .button_container{
    display:flex;
    gap:10px;
    
    @include breakpoint($PC){
      justify-content: center;
    }

    button{
      border:0;
      background-color: $light5;
    }

    .back{
      width:100px;
      height:60px;
      background:no-repeat url('./assets/img/Property 1=Back, Size=Small.png');
    
      @include breakpoint($PC){
        width:176px;
        height:82px;
        background:no-repeat url('./assets/img/Property 1=Back, Size=Large.png');
      }
    }

    .submit{
      width:180px;
      height:60px;
      background:no-repeat url('./assets/img/Property 1=Default, Size=Medium.png');
    
      @include breakpoint($PC){
        width:176px;
        height:82px;
        background:no-repeat url('./assets/img/Property 1=Default, Size=Large.png');
      }
    }
  }
  .modal{
    .modal-content{
      display: flex;
      padding:60px 67px;
      border-radius: 80px;

      @include breakpoint($PC){
        width:600px;
        height: 400px;
        padding: 71px 192px;
      }
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
        border: 0;
        width:100px;
        height:60px;
        background:no-repeat url('./assets/img/Property 1=Back, Size=Small.png');
    
        @include breakpoint($PC){
          width:176px;
          height:82px;
          background:no-repeat url('./assets/img/Property 1=Back, Size=Large.png');
        }
      }
    }
  }
}

.public_feedback_container{
  padding: 20px 15px 130px;
  text-align: center;
  @include breakpoint($PC){
    display:flex;
    padding: 30px 219px 60px 156px;
  }
  
  .public_feedback_title_text_img_small{
    margin-bottom: 10px;
    @include breakpoint($PC){
      display:none;
    }
  }

  .public_feedback_title_text_img_large{
    display:none;
    @include breakpoint($PC){
      display:block;
    } 
  }

  .public_feedback_description{
    @include breakpoint($PC){
      display: flex;
      flex-direction: column;
      align-items: center;
      gap:20px;
      width: 679px;
      padding:0 100px;
    }
  }

  .public_feedback_text{
    margin-bottom: 15px;
    font-size: $font_normal;
    @include breakpoint($PC){
      margin-bottom: 0;
      font-size: 24px;
      font-weight: 700; 
    }
  }

  .public_feedback_slogan{
    margin:0;
    @include breakpoint($PC){
      font-size: 24px;
      font-weight: 700;
    }
  }

  .form_content{
    display: flex;
    flex-direction: column;
    gap:10px;
    @include breakpoint($PC){
      flex-grow: 1;
      padding-top: 30px;
    }  
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

      @include breakpoint($PC){
        padding:45px 38px;    
      }
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

      button{
        border: 0;
        width:100px;
        height:60px;
        background:no-repeat url('./assets/img/Property 1=Back, Size=Small.png');
    
        @include breakpoint($PC){
          width:176px;
          height:82px;
          background:no-repeat url('./assets/img/Property 1=Back, Size=Large.png');
        }
      }
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
  top: -120.864px;
  left: 18px;
  @include breakpoint($PC){
    top:-181.229px;
    left: 240px;
  }
    
    img{
    width: 355px;

    @include breakpoint($PC){
      width: 530px;
    }
  }
}

footer{
  padding:30px 21px 15px;
  position: relative;
  @include breakpoint($PC){
    padding:15px 156px;
    display:flex;
    flex-wrap: wrap;
  }
}

.candidate_name_text_img{
  display: none;
  @include breakpoint($PC){
    display: block;
    margin-top: 23px;
    margin-right:318px;
  }
}
.menu{
  margin-bottom: 60px;
  text-align: center;
  @include breakpoint($PC){
    flex-grow: 100%;
    margin-right: 60px;
    margin-bottom: 0;
  }
  &_title{
    display:block;
    margin-bottom: 10px;
    font-size: $font_small;
    color:$secondary_orange;
  }

  &_link{
    display: flex;
    justify-content: center;
    gap:50px;

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
  @include breakpoint($PC){
    flex-grow: 30%;
  }
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
      font-size: $font_normal;
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

  @include breakpoint($PC){
    flex-grow: 1;
  }
}

</style>
