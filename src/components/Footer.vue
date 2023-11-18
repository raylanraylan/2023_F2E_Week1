<script setup></script>
<template>
  <footer data-aos="fade-up">
    <div class="cat_img">
      <img src="../assets/img/Mokker (6) 1.png" alt="貓咪照片"> 
    </div>
    <a href="#" class="candidate_name_text_img">
      <img class="candidate_name" src="../assets/img/Logo (1).png" alt="候選人名字">
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