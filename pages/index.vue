<template>
  <div
    class="container"
    style="margin-top: 70px;"
  >
    <div class="mb-3">
      <input
        v-model="busca"
        class="form-control mr-sm-2"
        type="text"
        placeholder="Buscar vagas"
        aria-label="Buscar vagas"
      >
    </div>
    <div class="row">
      <div
        v-for="(job, i) in filtro_vagas"
        :key="i"
        class="col-sm-4 pb-3"
      >
        <a href="#" style="text-decoration: none;">
          <div class="card text-center" style="height: 100%;">
            <img v-if="job.url_banner" :src="job.url_banner" class="card-img-top" alt="">
            <img v-else src="https://web-static.hunterco.com.br/banners/private-company.png" class="card-img-top" alt="">

            <div class="card-body">
              <div class="card-title">
                <h4>{{ job.vaga }}</h4>
                <h5>{{ job.nome_empresa }} - {{ job.cidade }}</h5>
                <h6>{{ job.area }} - {{ job.senioridade }} - R$ {{ job.valor }}</h6>
              </div>

              <p class="card-text">
                <span
                  class="badge badge-primary mx-1"
                  v-for="(tag, i) in job.tags"
                  :key="i"
                  v-if="tag"
                >
                  {{ tag }}
                </span>
              </p>
            </div>
          </div>
        </a>
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
      busca: ''
    }
  },

  computed: {
    filtro_vagas: function() {
      return this.jobs.filter(job => job.vaga.toLowerCase().match(this.busca.toLowerCase()))
    }
  }
}
</script>

<style>
</style>
