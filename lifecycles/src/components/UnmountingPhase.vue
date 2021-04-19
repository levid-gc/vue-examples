<template>
  <div>
    <div>
      <input type="checkbox" v-model="checked" />
      <label>Checkbox</label>
    </div>
    <p>Checked Value: {{ checked }}</p>
    <div v-if="checked">
      <MessageDisplay />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MessageDisplay from './MessageDisplay.vue';

const UnmountingPhase = defineComponent({
  components: {
    MessageDisplay
  },

  data() {
    return {
      checked: true
    };
  }
});

export default UnmountingPhase;
</script>
