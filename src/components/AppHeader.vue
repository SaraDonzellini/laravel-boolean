<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      links: [
        {
          name: 'HomePage',
          route: 'homepage'
        },
        {
          name: 'Library',
          route: 'library'
        },
        {
          name: 'About Us',
          route: 'aboutUs'
        },
        {
          name: 'Contact Us',
          route: 'contactUs'
        },
      ]
    }
  },
}
</script>

<template lang="">
  <header class='container-fluid'>
    <section class="row">
      <div class="col-12 p-0">
        <nav class="navbar navbar-expand-lg bg-light">
          <div class="container">
            <a class="navbar-brand" href="#">Library</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                <li class="nav-item" v-for="link in links">
                  <router-link :to="{name : link.route}" class="nav-link">{{link.name}}</router-link>
                </li>
              </ul>

            </div>
          </div>
        </nav>
      </div>
    </section>
  </header>
</template>

<style lang="">
  
</style>

