<template>
  <Header />
  <main class="main">
    <div class="main__gases">
      <div class="container">
        <h2 class="main__gases-title">{{ $t("gases.title") }}</h2>
        <div class="main__gases-block">
          <div class="main__gases-item" v-for="item in gases" :key="item.id">
            <img :src="item.img" alt="" class="main__gases-img" />
            <h2 class="main__gases-block_title">
              {{ item.title }}
            </h2>
            <p class="main__gases-block_text">
              {{ item.text }}
            </p>
            <router-link
              :to="/gases/ + item.id"
              class="main__gases-link arrow-right"
              >{{ $t("gases.more") }}</router-link
            >
          </div>
        </div>
      </div>
    </div>
    <MainCommunication />
  </main>
  <Footer />
</template>

<script>
import Header from "@/components/Header.vue";
import MainCommunication from "@/components/MainCommunication.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: { MainCommunication, Footer, Header },
  data() {
    return {
      gases: [
        {
          id: 1,
          img: require("@/assets/img/gases.png"),
          title: this.$t("gases.gasesOne.title"),
          text: this.$t("gases.gasesOne.text"),
        },
        {
          id: 2,
          img: require("@/assets/img/gases.png"),
          title: this.$t("gases.gasesTwo.title"),
          text: this.$t("gases.gasesTwo.text"),
        },
        {
          id: 3,
          img: require("@/assets/img/gases.png"),
          title: this.$t("gases.gasesThree.title"),
          text: this.$t("gases.gasesThree.text"),
        },
      ],
    };
  },
};
</script>

<style>
</style>
