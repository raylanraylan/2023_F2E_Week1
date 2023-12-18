<script setup>
import { ref } from 'vue'
const formInputs = ref('');
const submit = ()=>{
  // const form

  // for(const node of formContent.value.childNodes){
  //   node
  // }
}
</script>
<template>
  <section class="public_feedback" id="public_feedback">
    <form class="public_feedback_container">
      <div class="public_feedback_description">
        <div class="public_feedback_title_text_img_small"><img src="@/assets/img/feedback.png"></div>
        <div class="public_feedback_title_text_img_large"><img src="@/assets/img/feedback_large.png"></div>
        <h5 class="public_feedback_slogan">您的聲音，我們的行動！</h5>
        <p class="public_feedback_text">親愛的鄉親，每一位市民的意見都是我們社區前進的原動力。無論大小事，我都誠摯希望聽到您的建議。分享您的想法，一同為我們的未來打造更美好！</p>
      </div>
      <div class="form_content">
        <div class="form_inputs" ref="formInputs">
          <input type="text" class="form-control" id="nameInput" placeholder="您的姓名" required>
          <input type="email" class="form-control" id="emailInput" placeholder="您的Email" required>
          <input type="tel" class="form-control" id="phoneInput" placeholder="您的手機" required>
          <textarea class="form-control" id="messageInput" placeholder="您的建言" required></textarea>
        </div>
        <button type="button" @click="submit" class="btn btn-primary public_feedback_submit" data-bs-toggle="modal" data-bs-target="#feedbackSubmit">
          <img src="@/assets/img/submit.png" alt="送出意見的按鍵">
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
</template>
<style lang="scss">
.public_feedback{
  background-color: #E3E3E3;
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
    gap:20px;
    @include breakpoint($PC){
      flex-grow: 1;
      padding: 30px 97px;
    }
  }
  
  .form_inputs{
    display: flex;
    flex-direction: column;
    gap:10px;
  }

  .form-control,label{
    padding: 10px;
    font-size: $font_normal;
  }

  .form-control{
    &:focus-visible{
      border: 1px solid $light2;
      box-shadow:none;
    }
    &:invalid{
      border: 1px solid #FF3B3B;
    }
    &::placeholder{
      color:#C1C1C1;
    }
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
    padding: 0;
    background-color: #E3E3E3;

    &:hover{
      background-color: #E3E3E3;
    }
  }

  //去掉btn背景
  :not(.btn-check) + .btn:active{
    background-color: #E3E3E3;
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
        background:no-repeat url('@/assets/img/Property 1=Back, Size=Small.png');
    
        @include breakpoint($PC){
          width:176px;
          height:82px;
          background:no-repeat url('@/assets/img/Property 1=Back, Size=Large.png');
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
</style>