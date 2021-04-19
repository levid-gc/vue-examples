<template>
  <div>
    <p>Update Phase</p>

    <div>
      Names:
      <ul>
        <li v-for="name in names" v-bind:key="name">
          {{ name }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const UpdatePhase = defineComponent({
  data() {
    return {
      checked: false,
      names: [] as string[]
    };
  },

  mounted() {
    this.checked = true;

    (this.$attrs['data-names'] as string)
      .split(',')
      .forEach(name => this.names.push(name));
  },

  beforeUpdate() {
    console.log(`beforeUpdate called. Checked: ${this.checked}, Name: ${this.names[0]}, List Elements: ${this.$el.getElementsByTagName('li').length}`);
  },

  updated() {
    console.log(`updated called. Checked: ${this.checked}, Name: ${this.names[0]}, List Elements: ${this.$el.getElementsByTagName('li').length}`);
  },

  watch: {
    checked(newVal, oldVal) {
      console.log(`Checked Watch, Old: ${oldVal}, New: ${newVal}`);
    }
  }
});

export default UpdatePhase;
</script>
