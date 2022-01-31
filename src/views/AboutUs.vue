<template>
<div class="wrapper">
  <h1>О нас</h1>
  <div class="anekdot">
   <p>Попали на необитаемый остров американец, немец и русский.<br>
   Однажды прибило к острову бутылку, открыли они ее, а оттуда - джинн:<br>
    - Вы меня освободили, я исполню по два ваших желания! <br>
    - Мешок денег и домой! - сказал американец и исчез.<br>
    - Кружку пива и домой! - сказал немец и был таков.<br>
    - Хорошая была компания, ящик водки и всех обратно! - сказал русский.</p>
  </div>
</div>
</template>

<script>
export default {
  name: "AboutUs"
}
</script>

<style scoped>
.wrapper {
  padding: 20px;
}
  .anekdot{
    display: block;
    margin: 10px;
    padding-top: 100px;
  }
  h1 {
    margin: 0;
    font-size: 30px;
    font-family: "Arial", sans-serif;
  }
</style>