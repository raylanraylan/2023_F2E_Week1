<script setup>
import { nextTick, onMounted,ref } from 'vue';
const straightChineseName = ref('');
const horizontalEnglishName = ref('');
onMounted(()=>{
  nextTick(()=>{
    window.addEventListener('scroll', () => {
      const initialChineseDistanceFromTop = 30;
      const chinesePositionY = window.scrollY - initialChineseDistanceFromTop
      straightChineseName.value.style.top = `${-chinesePositionY}px`

      const initialEnglishDistanceFromLeft = 53;
      const englishPositionX = initialEnglishDistanceFromLeft - window.scrollY
      horizontalEnglishName.value.style.left = `${englishPositionX}px`
    });
  })
})
</script>
<template>
    <section class="cover">
      <div class="cover_container">
        <h2 class="cover_slogan_phone">
          <div class="election_text_img">
            <img src="@/assets/img/2023_THE_F2E_legislative election.png" alt="宣傳標語：2023 the f2e 立委競選">
          </div>
          <div class="cat_eye_text_img">
            <img src="@/assets/img/Seeing Taiwan through the eyes of cats.png" alt="宣傳標語：從喵的眼中看見台灣">
          </div>
        </h2>
        <h2 class="cover_slogan_pc">
          <div class="election_text_img">
            <img src="@/assets/img/2023_THE_F2E_legislative election_PC.png" alt="宣傳標語：2023 the f2e 立委競選">
          </div>
          <div class="cat_eye_text_img">
            <img src="@/assets/img/Seeing Taiwan through the eyes of cats_PC.png" alt="宣傳標語：從喵的眼中看見台灣">
          </div>
        </h2>
        <div class="candidate">
            <img src="@/assets/img/candidate.png" alt="候選人照片">
          </div>
        <div class="cover_content">
          <div class="keep_it_possible_phone">
            <img src="@/assets/img/KEEP IT POSSIBLE.png" alt="宣傳標語：keep it possible">
          </div>
          <div class="keep_it_possible_pc">
            <img src="@/assets/img/Frame 1.png" alt="宣傳標語：keep it possible">
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
              <img src="@/assets/img/Miao Li-Han.png">
            </div>
            <div class="miao_Li-Han_text_img_pc" ref="horizontalEnglishName">
              <img src="@/assets/img/Miao Li-Han (1).png">
            </div>
            <div class="miao_Li-Han_text_straight_img" ref="straightChineseName">
              <img src="@/assets/img/Miao Li-Han_straight.png">
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
</template>
<style lang="scss">
//cover
.cover{
  background-color: #E3E3E3;
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

    .miao_Li-Han_text_straight_img{
      display: none;
      @include breakpoint($PC){
        display:block;
        position:absolute;
        top:30px;
        right:0;
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
    // height: 270px;
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
  width: 50%;
  position: absolute;
  left: 33%;
  bottom: 38%;

  @include breakpoint(520px){
    width: 40%;
    left: 50%;
    bottom: 33%;
  }

  @include breakpoint($tablet){
    width: 30%;
    bottom: 30%;
  }

  @include breakpoint(900px){
    width: 30%;
    bottom: 25%;
    left: 60%;
  }

  @include breakpoint(1024px){
    width: 25%;
  }

  @include breakpoint(1200px){
    width: 20%;
  }

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

</style>