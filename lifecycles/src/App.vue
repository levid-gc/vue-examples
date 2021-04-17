<template>
  <CreationPhase />
  <MountingPhase data-names="Bob, Alice, Peter, Dora" />
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import CreationPhase from './components/CreationPhase.vue';
import MountingPhase from './components/MountingPhase.vue';

const App = defineComponent({
  components: {
    CreationPhase,
    MountingPhase
  }
});

export default App;
</script>
