<template>
  <p>Creation Phase</p>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const CreationPhase = defineComponent({
  data() {
    return {
      checked: true
    };
  },

  beforeCreate() {
    console.log(`beforeCreate method called ${this.checked}`);
  },

  created() {
    console.log(`created method called ${this.checked}`);
  }
});

export default CreationPhase;
</script>

<style>

</style>
