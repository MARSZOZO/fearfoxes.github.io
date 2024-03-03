<template>
  <div id="app" class="app">
    <FearHeader button-close-name="РАЗДЕЛЫ" @modal="visibleModal" />
    <vue-book-effects
      class="fear-book"
      ref="bookEffects"
      :ambient="0"
      :gloss="0.1"
      :nPolygons="15"
      :pages="pages"
      :startPage="currentBookOptions.page"
      :loadingImage="require('@/assets/loader.svg')"
    />
    <FearLinks />
    <FearModal v-if="isVisibleDrawer" :chapters="chapters" @to="handleClickPushToPage">
      <template #title>
        <FearHeader button-close-name="ЗАКРЫТЬ" @modal="visibleModal" />
      </template>
    </FearModal>
  </div>
</template>

<script>
import VueBookEffects from "vue-book-effects";
import FearHeader from "@/components/FearHeader.vue";
import FearLinks from "@/components/FearLinks.vue";
import FearModal from "@/components/FearModal.vue";

export default {
  name: "App",
  components: {FearModal, FearLinks, FearHeader, VueBookEffects },
  data() {
    return {
      isVisibleDrawer: false,
      currentBookOptions: {
        page: 1,
        label: 'арты',
      },
      pages: [],
      chapters: [
        { label: 'обо мне', page: 2 },
        { label: 'графика', page: 4 },
        { label: 'наброски', page: 44 },
        { label: 'граффити', page: 46 },
        { label: 'арты', page: 50 },
        { label: 'живопись', page: 64 },
        { label: 'айдентика', page: 70 },
        { label: 'коммерческие проекты', page: 90 },
        { label: 'стикеры', page: 98 },
        { label: 'инфографика', page: 100 },
        { label: 'полиграфия', page: 104 },
      ]
    };
  },
  mounted() {
    window.addEventListener('keydown', ev => {
      const bookEffects = this.$refs.bookEffects
      if (!bookEffects) {
        return
      }
      if (ev.keyCode === 37 && bookEffects.canFlipLeft) {
        bookEffects.flipLeft()
      }
      if (ev.keyCode === 39 && bookEffects.canFlipRight) {
        return bookEffects.flipRight()
      }
    });

    setTimeout(() => {
      this.pages = [
        null,
        require("@/assets/pages/0-0.jpg"),
        require("@/assets/pages/0-1.jpg"),
        require("@/assets/pages/0-2.jpg"),
        require("@/assets/pages/1-графика.jpg"),
        require("@/assets/pages/2.jpg"),
        require("@/assets/pages/3.jpg"),
        require("@/assets/pages/4.jpg"),
        require("@/assets/pages/5.jpg"),
        require("@/assets/pages/6.jpg"),
        require("@/assets/pages/7.jpg"),
        require("@/assets/pages/8.jpg"),
        require("@/assets/pages/9.jpg"),
        require("@/assets/pages/10.jpg"),
        require("@/assets/pages/11.jpg"),
        require("@/assets/pages/12.jpg"),
        require("@/assets/pages/13.jpg"),
        require("@/assets/pages/14.jpg"),
        require("@/assets/pages/15.jpg"),
        require("@/assets/pages/16.jpg"),
        require("@/assets/pages/17.jpg"),
        require("@/assets/pages/18.jpg"),
        require("@/assets/pages/19.jpg"),
        require("@/assets/pages/20.jpg"),
        require("@/assets/pages/21.jpg"),
        require("@/assets/pages/22.jpg"),
        require("@/assets/pages/23.jpg"),
        require("@/assets/pages/24.jpg"),
        require("@/assets/pages/25.jpg"),
        require("@/assets/pages/26.jpg"),
        require("@/assets/pages/27.jpg"),
        require("@/assets/pages/28.jpg"),
        require("@/assets/pages/29.jpg"),
        require("@/assets/pages/30.jpg"),
        require("@/assets/pages/31.jpg"),
        require("@/assets/pages/32.jpg"),
        require("@/assets/pages/33.jpg"),
        require("@/assets/pages/34.jpg"),
        require("@/assets/pages/35.jpg"),
        require("@/assets/pages/36.jpg"),
        require("@/assets/pages/37.jpg"),
        require("@/assets/pages/38.jpg"),
        require("@/assets/pages/39.jpg"),
        require("@/assets/pages/40.jpg"),
        require("@/assets/pages/41-наброски.jpg"),
        require("@/assets/pages/42.jpg"),
        require("@/assets/pages/43-граффити.jpg"),
        require("@/assets/pages/44.jpg"),
        require("@/assets/pages/45.jpg"),
        require("@/assets/pages/46.jpg"),
        require("@/assets/pages/47-арты.jpg"),
        require("@/assets/pages/48.jpg"),
        require("@/assets/pages/49.jpg"),
        require("@/assets/pages/50.jpg"),
        require("@/assets/pages/51.jpg"),
        require("@/assets/pages/52.jpg"),
        require("@/assets/pages/53.jpg"),
        require("@/assets/pages/54.jpg"),
        require("@/assets/pages/55.jpg"),
        require("@/assets/pages/56.jpg"),
        require("@/assets/pages/57.jpg"),
        require("@/assets/pages/58.jpg"),
        require("@/assets/pages/59.jpg"),
        require("@/assets/pages/60.jpg"),
        require("@/assets/pages/61-живопись.jpg"),
        require("@/assets/pages/62.jpg"),
        require("@/assets/pages/63.jpg"),
        require("@/assets/pages/64.jpg"),
        require("@/assets/pages/65.jpg"),
        require("@/assets/pages/66.jpg"),
        require("@/assets/pages/67-айдентика.jpg"),
        require("@/assets/pages/68.jpg"),
        require("@/assets/pages/69.jpg"),
        require("@/assets/pages/70.jpg"),
        require("@/assets/pages/71.jpg"),
        require("@/assets/pages/72.jpg"),
        require("@/assets/pages/72-1.jpg"),
        require("@/assets/pages/73.jpg"),
        require("@/assets/pages/73-1.jpg"),
        require("@/assets/pages/74.jpg"),
        require("@/assets/pages/75.jpg"),
        require("@/assets/pages/76.jpg"),
        require("@/assets/pages/77.jpg"),
        require("@/assets/pages/78.jpg"),
        require("@/assets/pages/79.jpg"),
        require("@/assets/pages/80.jpg"),
        require("@/assets/pages/81.jpg"),
        require("@/assets/pages/82.jpg"),
        require("@/assets/pages/83.jpg"),
        require("@/assets/pages/84.jpg"),
        require("@/assets/pages/85-коммерческие-проекты.jpg"),
        require("@/assets/pages/86.jpg"),
        require("@/assets/pages/87.jpg"),
        require("@/assets/pages/88.jpg"),
        require("@/assets/pages/89.jpg"),
        require("@/assets/pages/90.jpg"),
        require("@/assets/pages/91.jpg"),
        require("@/assets/pages/92.jpg"),
        require("@/assets/pages/93-стикеры.jpg"),
        require("@/assets/pages/94.jpg"),
        require("@/assets/pages/95-инфография.jpg"),
        require("@/assets/pages/96.jpg"),
        require("@/assets/pages/97.jpg"),
        require("@/assets/pages/98.jpg"),
        require("@/assets/pages/99-полиграфия.jpg"),
        require("@/assets/pages/100.jpg"),
        require("@/assets/pages/101.jpg"),
        require("@/assets/pages/102.jpg"),
        require("@/assets/pages/103.jpg"),
        require("@/assets/pages/финальная.jpg"),
      ]
    }, 1)
  },
  methods: {
    handleClickPushToPage({ page, label }) {
      this.currentBookOptions.page = page;
      this.currentBookOptions.label = label;

      this.$nextTick(() => {
        this.visibleModal();
      })
    },
    visibleModal() {
      this.isVisibleDrawer = !this.isVisibleDrawer;
    },
  }
};
</script>

<style>
@font-face {
  font-family: MyFont;
  src: url("@/assets/font/centurygothic_bold.ttf");
}

html,
body {
  margin: 0;
  padding: 0;
  font-family: centurygothic, sans-serif;
}

.app {
  position: relative;
  background: url("@/assets/fear_background.png") no-repeat;
  background-size: cover;
  object-fit: contain;
  display: flex;
  flex-direction: column;
}

.app__content {
  padding: 120px 60px 90px 60px;
  overflow: hidden;
}


.fear-book {
  padding: 0 60px;
  height: calc(100vh - 123px - 84px);
}

.fear-book .bounding-box {
  box-shadow: 0 0 20px #000;
}

@media (max-width: 767.98px) {
  .fear-book {
    padding: 0 20px;
    height: calc(100vh - 76px - 70px);
  }
}

</style>
