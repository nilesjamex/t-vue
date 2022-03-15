<template>
  <div class="home">
    {{ jobs[0].name }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from 'vue';
import Job from '@/types/job'
 // @ is an alias to /src

export default defineComponent({
  name: 'HomeView',
  components: {
  },
  setup() {
    const jobs = ref(<Job[]>[
      {
        title: 'jay jay',
        location: 'bad man town',
        salary: 30000,
        id: 1
    },
     {
        title: 'jay say',
        location: 'man town',
        salary: 60000,
        id: 2
    },
     {
        title: 'jay pryy',
        location: 'bad man town',
        salary: 40000,
        id: 3
    }
    ])

    return { jobs}
  }
});
</script>
