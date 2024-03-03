<template>
  <div class="modal-backdrop">
    <div class="modal">
      <section class="modal-body">
        <div class="app__modal">
          <div class="app__modal-chapters">
            <div
                class="app__modal-chapter"
                v-for="(chapter, i) in chapters"
                :key="i"
                @click="$emit('to', chapter)"
            >
              {{ chapter.label }}
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FearModal',
  props: {
    chapters: Array,
  },
  methods: {
    close() {
      this.$emit('close');
    },
  },
};
</script>

<style>
.app__modal {
  display: flex;
  justify-content: space-between;
}

.app__modal-chapters {
  display: flex;
  flex-wrap: wrap;
  text-transform: uppercase;
  gap: 50px;
}

.app__modal-chapter {
  font-size: 64px;
  font-weight: bold;
  width: fit-content;
  cursor: pointer;
  transition: .5s ease;
}

.app__modal-chapter:hover {
  color: #8200ff;
}


.modal-backdrop {
  position: fixed;
  top: 123px;
  bottom: 85px;
  left: 0;
  right: 0;
}

.modal {
  overflow-x: auto;
  display: flex;
  flex-direction: column;
  height: 100%;
  position: relative;
}

.modal-body {
  position: relative;
  padding: 0 60px 0 60px;
}
</style>
