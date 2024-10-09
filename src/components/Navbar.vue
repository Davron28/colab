<template>
  <nav class="header__nav">
    <router-link to="/" class="header__logo">
      <img src="@/assets/img/logo.png" alt="" />
    </router-link>
    <ul class="header__nav-list" :class="{ active: !burger }">
      <li>
        <router-link to="/" class="header__nav-link">{{ $t("headerLink.company") }}</router-link>
      </li>
      <li>
        <router-link to="/clean" class="header__nav-link">{{ $t("headerLink.clean") }}</router-link>
      </li>
      <li>
        <router-link to="/gases" class="header__nav-link">{{ $t("headerLink.gases") }}</router-link>
      </li>
      <li>
        <router-link to="/info" class="header__nav-link">{{ $t("headerLink.info") }}</router-link>
      </li>
      <li>
        <a href="#!" class="header__nav-lang" :class="{ active: !burger }" @click="changeLang">{{ $t("lang") }}</a>
      </li>
      <li
        class="header__burger-line_list"
        :class="{ active: !burger }"
        @click="burger = !burger"
      >
        <span class="icon__close"></span>
      </li>
    </ul>
    <div class="header__nav-contacts">
      <a href="tel:998901111137" class="header__nav-contact icon__call"
        > + 998 90 111 11 37</a
      >
      <a href="mailto:info@labsnab.uz" class="header__nav-contact icon__email"
        >  info@labsnab.uz</a
      >
    </div>
    <div
      class="header__burger"
      @click="burger = !burger"
      :class="{ active: !burger }"
    >
      <span class="header__burger-line"></span>
      <span class="header__burger-line"></span>
      <span class="header__burger-line"></span>
    </div>
  </nav>
</template>

<script>
import { useI18n } from 'vue-i18n';
export default {
  setup() {
    const { t, locale } = useI18n({useScope: "global"});
    const changeLang = () => {
      locale.value === "en" ? locale.value = "ru" : locale.value = "en"
      localStorage.setItem("lang", locale.value)
    }
    return { t, changeLang };
  },
  data() {
    return {
      burger: true,
    };
  },
};
</script>

<style>
</style>