<template>
  <header class="header__gases">
    <div class="container">
      <Navbar />
    </div>
  </header>
  <main class="main">
    <div class="container">
      <div class="main__gases-current">
        <h2 class="main__gases-current_title">{{ getGases.title }}</h2>
        <div class="main__gases-current_left">
          <img src="@/assets/img/статья.png" alt="" />
        </div>
        <div class="main__gases-current_right">
          <p class="main__gases-current_text">
            {{ $t("gases.info") }}
          </p>
        </div>
      </div>
    </div>
  </main>
  <Footer />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Navbar,
    Footer,
  },
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
      currentId: null,
    };
  },
  created() {
    this.currentId = this.$route.params.id;
  },
  computed: {
    getGases() {
      return this.gases.find((gases) => gases.id == this.currentId);
    },
  },
};
</script>

<style>
</style>