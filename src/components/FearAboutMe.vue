<template>
  <div class="drawer">
    fdsfdsf
  </div>
</template>

<style>
.drawer {
  position: fixed;
  z-index: 1;
  bottom: 0;
  top: -100%;
  height: 100%;
  background-color: black;
  overflow-x: hidden;
  transition: 0.2s;
  display: flex;
  flex-direction: column;
  width: 100vw;
}

.drawer.open {
  top: 0;
}

</style>