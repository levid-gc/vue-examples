<template>
  <div>
    <p>Count: {{ counter }}</p>
    <button @click="handleIncrement">Increment</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const MessageDisplay = defineComponent({
  data() {
    return {
      counter: 0
    };
  },

  created() {
    console.log('MessageDisplay: created');
  },

  beforeUnmount() {
    console.log('MessageDisplay: beforeUnmount');
  },

  unmounted() {
    console.log('MessageDisplay: unmounted');
  },

  methods: {
    handleIncrement() {
      this.counter += 1;
    }
  }
});

export default MessageDisplay;
</script>
