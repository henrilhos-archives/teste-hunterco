<template>
  <div>
    <nav
      class="navbar navbar-expand-md fixed-top"
      style="border-bottom: 1px solid #e7e7e7 !important;"
    >
      <a
        class="navbar-brand"
        href="#"
      >HunterConnect</a>

      <div
        id="navbarCollapse"
        class="collapse navbar-collapse"
      >
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <a
              class="nav-link"
              href="#"
            >
              Vagas
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              href="https://br.vuejs.org/"
              target="_blank"
            >
              VueJs
            </a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link"
              href="https://nuxtjs.org/"
              target="_blank"
            >
              NuxtJs
            </a>
          </li>
        </ul>

        <form class="form-inline mt-2 mt-md-0">
          <input
            class="form-control mr-sm-2"
            type="text"
            placeholder="Buscar vagas"
            aria-label="Buscar vagas"
          >
          <button class="btn btn-outline-primary my-2 my-sm-0">
            Buscar
          </button>
        </form>
      </div>
    </nav>

    <nuxt />
  </div>
</template>

<style>
</style>
