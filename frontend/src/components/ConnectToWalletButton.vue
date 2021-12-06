<template>
  <t-nav-button
    @click="onConnect"
  >
    Liên kết với Ví
  </t-nav-button>
</template>
<script>
import eventBus from '@/utils/eventBus';

export default {
  name: 'ConnectToWalletButton',
  methods: {
    onConnect() {
      eventBus.$emit('open-select-wallet');
    }
  }
};
</script>
