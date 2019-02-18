<template>
  <div>
    <nav class="navbar navbar-expand-md fixed-top shadow-lg">
      <a class="navbar-brand text-dark" href="#">HunterConnect</a>

      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarCollapse">
          <span class="fas fa-bars"></span>
      </button>

      <div id="navbarCollapse" class="collapse navbar-collapse">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <a class="nav-link" href="#">
              Vagas
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://br.vuejs.org/" target="_blank">
              VueJs
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://nuxtjs.org/" target="_blank">
              NuxtJs
            </a>
          </li>
        </ul>

        <div class="mt-2 mt-md-0">
          <i class="fas fa-home"></i>
        </div>
      </div>
    </nav>

    <div class="jumbotron jumbotron-fluid mt-4 bg-light">
      <div class="container">

        <div class="row">
          <div class="col-12 text-center mb-3">

              <h1 class="display-4">HunterCo</h1>
              <p class="lead">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Phasellus ultricies, metus et volutpat dapibus, ligula mauris imperdiet nisl, quis porta libero ligula ac leo.
                Mauris feugiat bibendum dolor eget interdum. Ut tristique eleifend dictum. Vestibulum non laoreet mauris.
                Nullam suscipit nisl lacus, quis condimentum leo finibus sit amet.
              </p>

              <hr>

          </div>
        </div>

        <div class="row">
          <div class="col-12">

            <ul class="nav nav-pills justify-content-center mb-4" id="pillsNav" role="tablist">

              <li class="nav-item">
                <a class="nav-link active" href="#navItem01" id="navpills01" data-toggle="pill">Diwe</a>
              </li>

              <li class="nav-item">
                <a class="nav-link" href="#navItem02" id="navpills02" data-toggle="pill">Oxygen</a>
              </li>

              <li class="nav-item">
                <a class="nav-link" href="#navItem03" id="navpills03" data-toggle="pill">Hydra</a>
              </li>

            </ul>

            <div class="tab-content" id="navPillsContent">
              <div class="tab-pane fade show active" id="navItem01" role="tabpanel">

                <div class="row">

                  <div class="col-sm-4">
                    <img src="https://web-static.hunterco.com.br/banners/diwe.png" class="img-fluid" alt="Imagem responsiva">
                  </div>

                  <div class="col-sm-8">
                    <p class="lead">
                      Aliquam velit ipsum, imperdiet eget orci vel, tempus ultrices diam.
                      Aliquam finibus sapien sed erat convallis, non consectetur nunc aliquam.
                      Cras cursus elit imperdiet, vehicula lacus nec, pulvinar tortor. Cras et tincidunt lorem.
                      Ut venenatis pellentesque libero vel ultricies. Maecenas imperdiet mattis nisi vel pellentesque.
                      Curabitur erat urna, consequat et ipsum eu, interdum tempus velit. Pellentesque consectetur interdum nibh ut mattis.
                      Sed sollicitudin ante vel enim pretium interdum.
                    </p>
                  </div>

                </div>

              </div>
              <div class="tab-pane fade" id="navItem02" role="tabpanel">

                <div class="row">

                  <div class="col-sm-4">
                    <img src="https://web-static.hunterco.com.br/banners/oxygen-systems.png" class="img-fluid" alt="Imagem responsiva">
                  </div>

                  <div class="col-sm-8">
                    <p class="lead">
                      Aliquam ornare, nunc sed sagittis ultrices, risus nunc lacinia sem, dignissim accumsan orci lacus et neque.
                      Duis a mollis orci, non vulputate purus. Sed tincidunt suscipit efficitur. Aenean a vestibulum odio.
                      Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Pellentesque vel tellus eu diam porta ultrices.
                      Mauris pretium accumsan neque, id aliquet dolor hendrerit sit amet. Duis eleifend nulla et volutpat porttitor.
                    </p>
                  </div>

                </div>

              </div>
              <div class="tab-pane fade" id="navItem03" role="tabpanel">

                <div class="row">

                  <div class="col-sm-4">
                    <img src="https://web-static.hunterco.com.br/banners/hydra-systems.png" class="img-fluid" alt="Imagem responsiva">
                  </div>

                  <div class="col-sm-8">
                    <p class="lead">
                      Nunc aliquam lorem varius, consectetur mauris sit amet, sodales nulla.
                      Aliquam ultrices, arcu vel volutpat condimentum, felis metus aliquam sem, in euismod urna augue a lectus.
                      In in efficitur magna, et convallis ligula. Vestibulum id est hendrerit, ultricies eros ut, dictum elit.
                      Suspendisse a venenatis felis, quis sagittis leo. Vestibulum rutrum lobortis felis sit amet cursus.
                    </p>
                  </div>

                </div>

              </div>

            </div>

          </div>
        </div>

      </div>
    </div>

    <nuxt />
  </div>
</template>

<style>
</style>
