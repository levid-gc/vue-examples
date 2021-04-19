<template>
  <!-- <CreationPhase />
  <MountingPhase data-names="Bob, Alice, Peter, Dora" />
  <UpdatePhase data-names="Bob, Alice, Peter, Dora" /> -->
  <UnmountingPhase />
</template>

<script lang="ts">
import { defineComponent } from 'vue';

// import CreationPhase from './components/CreationPhase.vue';
// import MountingPhase from './components/MountingPhase.vue';
// import UpdatePhase from './components/UpdatePhase.vue';
import UnmountingPhase from './components/UnmountingPhase.vue';

const App = defineComponent({
  components: {
    // CreationPhase,
    // MountingPhase,
    // UpdatePhase,
    UnmountingPhase
  }
});

export default App;
</script>
