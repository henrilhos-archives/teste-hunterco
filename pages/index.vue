<template>
  <div
    class="container"
    style="margin-top: 70px;"
  >
    <!-- seu código aqui -->

    <div
      v-for="(job, i) in jobs"
      :key="i"
    >
      {{ job }}
    </div>
  </div>
</template>

<script>
import Jobs from '@/components/jobs.js'
export default {
  data() {
    return {
      jobs: Jobs.getJobs()
    }
  },
}
</script>

<style>




</style>
