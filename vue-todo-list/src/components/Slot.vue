<template>
  <ModalDialog>
    <template v-slot:title>
      <span style="color: red">タイトル（赤）</span>
    </template>

    <template v-slot:default>
      <p>1. タイアログの内容</p>
      <p>2. タイアログの内容</p>
    </template>
  </ModalDialog>
</template>

<script>
import ModalDialog from './ModalDialog.vue';
export default {
  components: { ModalDialog },
};
</script>
