<script setup lang="ts">
import code from '@code-wallet/elements';
import { onMounted, ref } from 'vue'

const el = ref(null);

onMounted(() => {
  const { button } = code.elements.create('button', {
    currency: 'usd',
    destination: 'E8otxw1CVX9bfyddKu3ZB3BVLa4VVF9J7CTPdnUwT9jR',
    amount: 0.05,
  });

  button.mount(el.value);
})
</script>

<template>
  <div ref="el"></div>
</template>