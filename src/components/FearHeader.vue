<template>
  <div class="fear-header">
    <div class="fear-header__logo">
      <img src="@/assets/logo.svg" alt="Logo" />
    </div>
    <div class="fear-header__burger" @click="$emit('modal')">
      {{ buttonCloseName }}
    </div>
  </div>
</template>

<script>
export default {
  name: "FearHeader",
  props: {
    buttonCloseName: String,
  }
}
</script>

<style>
.fear-header {
  display: flex;
  justify-content: space-between;
  padding: 30px 60px 30px 60px;
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
}

.fear-header__logo {
  margin-left: calc(50% - 30px);
}

.fear-header__burger {
  font-size: 55px;
  line-height: 1;
  cursor: pointer;
  font-weight: bold;
  color: transparent;
  transition: .5s ease;
  -webkit-text-stroke: 2px #000000;
}

.fear-header__burger:hover {
  -webkit-text-stroke: 2px #8200ff;
}
</style>