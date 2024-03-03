<template>
  <el-dialog fullscreen :show-close="false" visible>
    <template #title>
      <slot name="title" />
    </template>
    <template #default>
      <div class="fear-modal__chapters">
        <div
            class="fear-modal__chapter"
            v-for="(chapter, i) in chapters"
            :key="i"
            @click="$emit('to', chapter)"
        >
          {{ chapter.label }}
        </div>
      </div>
    </template>
    <template #footer>
      <FearLinks />
    </template>
  </el-dialog>
</template>

<script>
import FearLinks from "@/components/FearLinks.vue";

export default {
  name: 'FearModal',
  components: { FearLinks},
  props: {
    chapters: Array,
  },
};
</script>

<style>
.el-dialog__header {
  padding: 0;
}
.el-dialog__footer {
  padding: 0;
}
.el-dialog__body {
  padding: 0 20px;
  color: #000000;
  height: calc(100% - 123px - 84px);
}

.fear-modal__chapters {
  display: flex;
  flex-wrap: wrap;
  text-transform: uppercase;
  gap: 50px;
}
.fear-modal__chapter {
  font-size: 64px;
  font-weight: bold;
  width: fit-content;
  cursor: pointer;
  transition: .5s ease;
  word-break: normal;
}
.fear-modal__chapter:hover {
  color: #8200ff;
}

@media (max-width: 767.98px) {
  .el-dialog__body {
    overflow-y: auto;
    height: calc(100% - 145px);
  }

  .fear-modal__chapters {
    flex-direction: column;
    flex-wrap: nowrap;
    gap: 20px;
  }
  .fear-modal__chapter {
    font-size: 35px;
  }
}
</style>
