<template>
  <div class="home">
    <button @click="handleClick('title')">order by title</button>
    <button @click="handleClick('location')">order by location</button>
    <button @click="handleClick('salary')" >order by salayr</button>
    <JobList :jobs="jobs" :order="order" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from "vue";
import JobList from "@/components/JobList.vue";
import Job from "@/types/job"
import OrderTerm from "@/types/OrderTerm"
// @ is an alias to /src

export default defineComponent({
  name: "HomeView",
  components: {
    JobList,
  },
  setup() {
    const jobs = ref(<Job[]>[
      {
        title: "jay jay",
        location: "bad man town",
        salary: 30000,
        id: 1,
      },
      {
        title: "jay say",
        location: "man town",
        salary: 60000,
        id: 2,
      },
      {
        title: "jay pryy",
        location: "bad man town",
        salary: 40000,
        id: 3,
      },
    ]);
    const order = ref<OrderTerm>('title')
    const handleClick = (term: OrderTerm) => {
      order.value = term
    }

    return { jobs, handleClick, order };
  },
});
</script>
