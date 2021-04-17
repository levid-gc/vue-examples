<template>
  <p>Mounting Phase</p>

  <div>
    Names:
    <ul>
      <li v-for="name in names" v-bind:key="name">
        {{ name }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const MountingPhase = defineComponent({
  data() {
    return {
      names: [] as string[]
    };
  },

  mounted() {
    (this.$attrs['data-names'] as string).split(',')
      .forEach((name: string) => this.names.push(name));
  }
});

export default MountingPhase;
</script>
