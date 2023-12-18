<script setup>
import { onMounted,ref } from 'vue';
import counterUp from 'counterup2';

onMounted(()=>{
  const el = document.querySelector('.counter')
  counterUp( el, {
    duration: 1000,
    delay: 16,
  } )

  const test = document.querySelector('.donation')
})

const toggleDonation = ref(true);
const donationPlan = ref(null);
const donationAmount = ref(null);

const chooseDonationPlan = ((event)=>{
  donationPlan.value = event.target.dataset.id
  if (event.target.dataset.amount==='random') return;
  donationAmount.value = event.target.dataset.amount
})

const inputOtherAmount = ((event)=>{
  donationAmount.value = event.target.value;
})

// const checkRandom = ()=>{
//   if (donationAmount.value===' ') return true;
//   if (donationAmount.value) return true;
// }

</script>
<template>
    <section class="donation" id="donation">
      <div class="donation_container">
        <div class="donation_description" v-if="toggleDonation">
          <div class="donation_title_text_img_small">
            <img src="@/assets/img/small donation.png" alt="小額捐款">
          </div>
          <div class="donation_title_text_img_large">
            <img src="@/assets/img/small donation_large.png" alt="小額捐款">
          </div>
          <p class="donation_text">您的小筆捐款，是每隻毛孩未來的大大動力！</p>
          <div class="donation_totalAmount">
            <div class="donation_totalAmount_text_img_small">
              <img src="@/assets/img/total amount.png" alt="累積總金額">
            </div>
            <div class="donation_totalAmount_text_img_large">
              <img src="@/assets/img/total amount_large.png" alt="累積總金額">
            </div>
            <div class="counter"><span class="total_amount">NT$<span class="number">987,655,873</span></span></div>
          </div>
          <button type="button" class="donation_button_small" @click="toggleDonation = !toggleDonation">
            <img src="@/assets/img/Btn.png" alt="前往捐款">
          </button>
          <button type="button" class="donation_button_large" @click="toggleDonation = !toggleDonation">
            <img src="@/assets/img/Btn (1).png" alt="前往捐款">
          </button>
        </div>
        <form class="donation_content" v-else>
          <h4 class="donation_plan_title">選擇捐款方案</h4>
          <div class="donation_plan">
            <div class="plan" data-amount="600" data-id="amount_600" :class="{active:donationPlan==='amount_600'}" @click="chooseDonationPlan">
              <h6 data-amount="600" data-id="amount_600">喵星人之友</h6>
              <span class="amount" data-amount="600" data-id="amount_600">NT$600</span>
              <span class="sponsors_number" data-amount="600" data-id="amount_600">已有 9957 人贊助</span>
            </div>
            <div class="plan" data-amount="6000" data-id="amount_6000" :class="{active:donationPlan==='amount_6000'}" @click="chooseDonationPlan">
              <h6 data-amount="6000" data-id="amount_6000">喵星大使</h6>
              <span class="amount" data-amount="6000" data-id="amount_6000">NT$6000</span>
              <span class="sponsors_number" data-amount="6000" data-id="amount_6000">已有 2000 人贊助</span>
            </div>
            <div class="plan" data-amount="60000" data-id="amount_60000" :class="{active:donationPlan==='amount_60000'}" @click="chooseDonationPlan">
              <h6 data-amount="60000" data-id="amount_60000">喵星傳奇</h6>
              <span class="amount" data-amount="60000" data-id="amount_60000">NT$60000</span>
              <span class="sponsors_number" data-amount="60000" data-id="amount_60000">已有 9957 人贊助</span>
            </div>
            <div class="plan" data-amount="random" data-id="amount_random" :class="{active:donationPlan==='amount_random'}" @click="chooseDonationPlan">
              <h6 data-amount="random" data-id="amount_random">自訂捐款金額</h6>
              <input class="input_amount" data-id="amount_random" type="text" placeholder="請輸入捐款金額" @input="inputOtherAmount">
            </div>  
          </div>
          <div class="button_container">
            <button class="back" @click="toggleDonation = !toggleDonation"></button>
            <button class="submit" type="button" data-bs-toggle="modal" data-bs-target="#donationSubmit" @click="checkRandom"></button>
          </div>
          <div class="modal fade" id="donationSubmit" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-header">
                  <h4 class="modal-title fs-5" id="staticBackdropLabel">感謝您成為喵星大使</h4>
                </div>
                <div class="modal-body">
                  <div class="amount_text">
                    <img src="@/assets/img/donation.png" alt="捐款金額文字">
                  </div>
                  <span class="amount">NT$<span>{{ donationAmount }}</span></span>
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
</template>
<style lang="scss">
.donation{  
  display: flex;
  justify-content: center;
  align-items: center;
  padding:45px 20px;
  background: no-repeat center/cover url('@/assets/img/female-hand-with-cat-paw-kitten-s-paw-woman-finger-contrast-close-up 1.png');
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
  
    .plan.active{
        border:solid 2px $main_blue;
      }
    }
    .plan{
      display: flex;
      flex-direction: column;
      gap:5px;
      padding: 15px 3px;
      border:solid 2px $light1;
      border-radius:8px;
      background-color: $white;

      cursor: pointer;
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

        .input_amount{
          outline: none;
          @include breakpoint($PC){
            padding: 14px 12px;
          }

          // &:focus-visible{
          //   border: 1px solid $light2;
          // }
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
      gap:20px;
    }

    button{
      border:0;
      background-color: $light5;
    }

    .back{
      width:100px;
      height:60px;
      background:no-repeat url('@/assets/img/Property 1=Back, Size=Small.png');
    
      @include breakpoint($PC){
        width:176px;
        height:82px;
        background:no-repeat url('@/assets/img/Property 1=Back, Size=Large.png');
      }
    }

    .submit{
      width:180px;
      height:60px;
      background:no-repeat url('@/assets/img/Property 1=Default, Size=Medium.png');
    
      @include breakpoint($PC){
        width:222px;
        height:82px;
        background:no-repeat url('@/assets/img/Property 1=Default, Size=Large.png');
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
        background:no-repeat url('@/assets/img/Property 1=Back, Size=Small.png');
    
        @include breakpoint($PC){
          width:176px;
          height:82px;
          background:no-repeat url('@/assets/img/Property 1=Back, Size=Large.png');
        }
      }
    }
  }
}
</style>