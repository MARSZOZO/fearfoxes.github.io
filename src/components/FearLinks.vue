<template>
  <div class="fear__links">
    <div class="fear__link">
      <i class="fa-solid fa-envelope" />
      <a href="mailto:fearfoxesdesign@gmail.com" target="_blank">fearfoxesdesign@gmail.com</a>
    </div>
    <div class="fear__link">
      <i class="fa-brands fa-square-instagram" />
      <a href="https://www.instagram.com/fear_612_/" target="_blank">fear_612_</a>
    </div>
    <div class="fear__link">
      <i class="fa-brands fa-vk" />
      <a href="https://vk.com/id108847211" target="_blank">Alina Naumova</a>
    </div>
    <div class="fear__link">
      <i class="fa-brands fa-telegram" />
      <a href="https://t.me/fearfoxes" target="_blank">fearfoxes</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "FearLinks"
}
</script>

<style>
.fear__links {
  display: flex;
  justify-content: space-between;
  padding: 0 60px 30px 60px;
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
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
</style>