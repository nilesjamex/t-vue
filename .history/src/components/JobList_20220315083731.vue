<template>
    <div class="jobs--list">
        <ul>
            <li v-for="job in jobs" :key="job.id">
                <h2>
                    {{ job.title }} in {{ job.location }}
                </h2>
                <div class="salary">
                    <p>
                        {{ job.salary }} naira
                    </p>
                </div>
                <div class="desc">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Accusamus, sequi!
                </div>
            </li>
        </ul>
    </div>
</template>
<script lang="ts">
import { defineComponent, PropType } from 'vue'
import Job from '@/types/job'

export default defineComponent({
    props: {
        jobs: {
            required: true,
            type: Array as PropType<Job[]>
        }
    }
})
</script>

<style lang="scss" scoped>

</style>
