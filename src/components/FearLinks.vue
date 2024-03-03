<template>
  <div class="fear__links">
    <div class="fear__link" @click="clickToLink('mailto:fearfoxesdesign@gmail.com')">
      <i class="fa-solid fa-envelope" />
      <a href="mailto:fearfoxesdesign@gmail.com" target="_blank">fearfoxesdesign@gmail.com</a>
    </div>
    <div class="fear__link" @click="clickToLink('https://www.instagram.com/fear_612_/')">
      <i class="fa-brands fa-square-instagram" />
      <a href="https://www.instagram.com/fear_612_/" target="_blank">fear_612_</a>
    </div>
    <div class="fear__link" @click="clickToLink('https://vk.com/id108847211')">
      <i class="fa-brands fa-vk" />
      <a href="https://vk.com/id108847211" target="_blank">Alina Naumova</a>
    </div>
    <div class="fear__link" @click="clickToLink('https://t.me/fearfoxes')">
      <i class="fa-brands fa-telegram" />
      <a href="https://t.me/fearfoxes" target="_blank">fearfoxes</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "FearLinks",
  methods: {
    clickToLink(url) {
      window.open(url, '_blank');
    },
  },
}
</script>

<style>
.fear__links {
  display: flex;
  justify-content: space-between;
  padding: 30px 60px;
  position: sticky;
  bottom: 0;
}

.fear__link {
  display: flex;
  gap: 15px;
  align-items: center;
  font-weight: bold;
  cursor: pointer;
  transition: .5s ease;
}

.fear__link:hover, .fear__link > a:hover {
  color: #8200ff;
}

.fear__link > a {
  text-decoration: none;
  font-weight: bold;
  color: black;
  font-size: 20px;
  cursor: pointer;
  transition: .5s ease;
}

.fa-square-instagram, .fa-vk, .fa-telegram, .fa-envelope {
  font-size: 23px;
}

@media (max-width: 767.98px) {
  .fear__links {
    padding: 20px 30px;
    z-index: 1;
  }

  .fear__link > a {
    display: none;
  }

  .fa-square-instagram, .fa-vk, .fa-telegram, .fa-envelope {
    font-size: 30px;
  }
}
</style>