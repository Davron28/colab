<template>
  <header class="header__info">    
    <div class="container">
      <Navbar/>
    </div>
  </header>
  <main class="main">
    <div class="main__info">
    <div class="container">
      <h2 class="main__info-title">{{ $t("info.title") }}</h2>
      <div class="main__info-block">
        <div class="main__info-item">
          <h2 class="main__info-block_title">{{ $t("info.itemOne.title") }}</h2>
          <p class="main__info-block_text">{{ $t("info.itemOne.text") }}</p>
          <a href="#!" class="main__info-block_btn">{{ $t("info.read") }}</a>
        </div>
        <div class="main__info-item">
          <h2 class="main__info-block_title">{{ $t("info.itemTwo.title") }}</h2>
          <p class="main__info-block_text">{{ $t("info.itemTwo.text") }}</p>
          <a href="#!" class="main__info-block_btn">{{ $t("info.read") }}</a>
        </div>
        <div class="main__info-item">
          <h2 class="main__info-block_title">{{ $t("info.itemThree.title") }}</h2>
          <p class="main__info-block_text">{{ $t("info.itemThree.text") }}</p>
          <a href="#!" class="main__info-block_btn">{{ $t("info.read") }}</a>
        </div>
        <div class="main__info-item">
          <h2 class="main__info-block_title">{{ $t("info.itemFour.title") }}</h2>
          <p class="main__info-block_text">{{ $t("info.itemFour.text") }}</p>
          <a href="#!" class="main__info-block_btn">{{ $t("info.read") }}</a>
        </div>
      </div>
    </div>
    </div>
  </main>
  <Footer/>
  
</template>

<script>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';

export default {
  components: {
    Navbar,
    Footer,
  }
}
</script>

<style>

</style>