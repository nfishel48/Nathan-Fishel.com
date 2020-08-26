

<template>
  <div id ="content">
    <div>
      <script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
      <b-navbar class="main-nav">
          <template slot="brand">
              <b-navbar-item class="main-nav" tag="router-link" :to="{ path: '/' }">
                  <img
                      src="~/assets/css/logo.png"
                      alt="My logo"
                  > 
              </b-navbar-item>
          </template>
          <template slot="start" class="main-nav">
             
          </template>

          <template slot="end" class="main-nav">
               <b-navbar-item class="nav-item" tag="router-link" :to="{ path: '/home' }">
                  Home
              </b-navbar-item>
              <b-navbar-item class="nav-item" tag="router-link" :to="{ path: '/about' }">
                  About Me
              </b-navbar-item>
              <b-navbar-item class="nav-item" tag="router-link" :to="{ path: '/Blog' }">
                  Blog
              </b-navbar-item>
              <b-navbar-item class="nav-item"  tag="router-link" :to="{ path: '/portfolio' }">
                  Portflolio
              </b-navbar-item>
              <b-navbar-item class="main-nav"  tag="div" >
                  <div class="buttons">
                      <b-button class="button button is-link is-inverted" tag="router-link" :to="{ path: '/contact' }">
                          Contact Me
                      </b-button>
                  </div>
              </b-navbar-item>
          </template>
      </b-navbar>
       <b-message title="Attention!" type="is-danger" aria-close-label="Close message">
            This site is currently undergoing a redesign, but dont't worry all information is up to date. Some elements may be missplaced so please check back soon for the final version.
        </b-message>
  </div>

  <nuxt/>

<footer class="footer">
  <div class="content has-text-centered">
    <p>
      <strong>Bulma</strong> by <a href="https://jgthms.com">Jeremy Thomas</a>. The source code is licensed
      <a href="http://opensource.org/licenses/mit-license.php">MIT</a>. The website content
      is licensed <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY NC SA 4.0</a>.
    </p>
  </div>
</footer>

</div>   
</template>

<script>
export default {
      data () {
    return {
      title: 'Nathaniel Fishel',
      year: '2020'
    }
  },
  head () {
    return {
      title: this.title,
      
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' },
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' }
      ]

    }
  },
  methods: {
    getDate: function(){
     var year =  new Date().getFullYear();
     return year;
    }
  }


}
</script>