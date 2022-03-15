<template>
  <div class="home">
    {{ name }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue';
 // @ is an alias to /src

export default defineComponent({
  name: 'HomeView',
  components: {
  },
  setup() {
    const state = reactive({
      name: "james",
      age: 21 as string | number
    })
    return { ...toRefs(state) }
  }
});
</script>
