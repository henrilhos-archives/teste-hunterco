<template>
  <div
    class="container"
    style="margin-top: 70px;"
  >
    <!-- seu código aqui -->
    <div v-for="(job, i) in jobs" :key="i" id='vagas'>
      <div class='card'>
        <img :src='job.url_banner' class='card-img-top' alt='logo-empresa'/>
        <div class='card-body'>
          <h5 class='card-title'>{{ job.nome_empresa }} - {{ job.vaga }} ({{ job.senioridade }})</h5>
          <p>Área: {{ job.area }}</p>
          <p>Local: {{ job.cidade }}</p>
          <p>Salário: R$ {{ job.valor }}</p>
          <div v-if="job.tags.length > 0">
            <a href="#" v-for="(tag, i) in job.tags" :key="i" class="badge">{{ tag }}</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Jobs from '@/components/Jobs.js'

export default {
  data() {
    return {
      jobs: Jobs.getJobs(),
    }
  },
}
</script>

<style>
</style>
