    <template>
      <div class="container" style="margin-top: 70px;">

        <header class="container_header">

          <h3>Pesquise por Nome da vaga:</h3>

          <input class="form-control mr-sm-2" type="text" placeholder="Buscar vagas" aria-label="Buscar vagas"  v-model="search">

        </header>

         <!--seu código aqui-->
        <div class="row justify-content-sm-center">

          <div class="col-sm-6 col-md-4" v-for="(job, i) in vagasFiltradas" :key="i">

        <div class="card mb-5">

            <img class="card-img-top" :src=" job.url_banner " alt="Imagem de capa do card" v-if="job.url_banner" >
            <img src="https://web-static.hunterco.com.br/banners/private-company.png" alt="Imagem Vaga" class="card-img-top" v-if="!job.url_banner">

            <hr>

          <div class="card-body">

            <h5 class="card-title">{{ job.vaga }}</h5>
            <p class="card-text">{{ job.nome_empresa }} - Estão contratando na vaga de {{ job.vaga }}</p>

          </div>

          <div class="card-footer bg-white">
            <a href="#" class="btn btn-outline-info btn-lg btn-block" data-toggle="modal" :data-target="'#'+job.id">Conhecer</a>
          </div>

          <div class="modal fade" :id="job.id" tabindex="-1" role="dialog" aria-labelledby="TituloModalCentralizado" aria-hidden="true">

            <div class="modal-dialog modal-dialog-centered" role="document">

              <div class="modal-content">

                <div class="modal-header">

                  <h5 class="modal-title" id="TituloModalCentralizado">{{ job.vaga }} - {{ job.nome_empresa }}</h5>

                  <button type="button" class="close" data-dismiss="modal" aria-label="Fechar">
                    <span aria-hidden="true">&times;</span>
                  </button>

                </div>

                <div class="modal-body">

                  {{ job.nome_empresa }} está contratando {{ job.vaga }} {{ job.senioridade }}, para trabalhar na área de {{ job.area }}. <div v-if="job.tags.length">É preferivel skills em:

                  <ul>

                  <li v-for="(tag, i) in job.tags" :key="i" v-if="tag"> {{ tag }} </li>

                  </ul>

                </div>

                </div>

                <div class="modal-footer">

                  <button type="button" class="btn btn-secondary" data-dismiss="modal">Fechar</button>
                  <button type="button" class="btn btn-primary" disabled>Candidatar-se</button>

                </div>

              </div>

            </div>

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
          search: '',
        }
      },
      methods:{

      },
      computed:{
        vagasFiltradas:function(){

          return this.jobs.filter((job) =>{
            return job.vaga.match(this.search);
          })

        }

      }
    }
    </script>

    <style>
      body{
        background-color: #1b7979;
      }
      nav{
        background-color: #24bbbc;
      }
      .container_header{
        margin-bottom: 1em;
      }
      a{
        color: #f7f8fb;
      }
      .nav-item > .nav-link {
        color: #000;
      }
      .nav-link.active{
          background-color: cadetblue !important;
      }
      #navbarCollapse > .nav-item > .nav-link{
        color: #ffffff !important;
      }
    </style>
