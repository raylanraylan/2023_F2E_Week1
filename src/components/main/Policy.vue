<script setup></script>
<template>
  <section class="policy" id="policy">
    <div class="policy_title_text_img_small">
      <img src="@/assets/img/policy.png" alt="政策議題">
    </div>
    <div class="policy_title_text_img_large">
      <img src="@/assets/img/policy_large.png" alt="政策議題">
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
</template>
<style lang="scss" scoped>

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

    @include breakpoint($tablet){
      flex-direction: row;
      align-items:stretch;
      justify-content: center;
    }
  }

  .card{
    padding:15px;
    border-radius: 8px;
    background-color: $light5;
    @include breakpoint($tablet){
      flex:1;
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

</style>