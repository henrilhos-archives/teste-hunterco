<template>
  <div>
    <nav
      class="navbar navbar-expand-md fixed-top"
      style="border-bottom: 1px solid #e7e7e7 !important; background-color: #007bff;"
    >
      <a
        class="navbar-brand cor-texto" 
        href="#"
      >HunterConnect</a>

      <div
        id="navbarCollapse"
        class="collapse navbar-collapse "
      >
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <a
              class="nav-link cor-texto"
              href="#"
            >
              Vagas
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link cor-texto"
              href="https://br.vuejs.org/"
              target="_blank"
            >
              VueJs
            </a>
          </li>
          <li class="nav-item cor-texto">
            <a
              class="nav-link cor-texto"
              href="https://nuxtjs.org/"
              target="_blank"
            >
              NuxtJs
            </a>
          </li>
        </ul>
      </div>
    </nav>

    <nuxt />
  </div>
</template>

<style> 
  .cor-texto {
    color: white;
  }
  .cor-texto:hover {
  color:#DCDCDC;
  }
</style>
