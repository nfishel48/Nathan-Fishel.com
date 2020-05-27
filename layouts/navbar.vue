

<template>
  <div id ="content">
    <div>
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
              <b-navbar-item class="nav-item"  tag="router-link" :to="{ path: '/portfolio' }">
                  Portflolio
              </b-navbar-item>
              <b-navbar-item class="main-nav"  tag="div" >
                  <div class="buttons">
                      <b-button class="button button is-link is-inverted" tag="router-link" :to="{ path: '/contact' }">
                          <strong>Contact Me</strong>
                      </b-button>
                  </div>
              </b-navbar-item>
          </template>
      </b-navbar>
  </div>

  <nuxt/>

   <footer class="footer">
    <div class="content has-text-centered">
      <div class="columns"> 
        <div class="column">
          <a href="/sitemap">Sitemap </a><i class="fas fa-map-signs"></i> 
        </div>


        <div class="column"> 
          <div>
            
            <span class="icon">
              <a href="https://github.com/nfishel48">
              <i class="fab fa-github"></i>
              </a>
            </span>

            <span class="icon">
              <a href="https://www.linkedin.com/in/nathaniel-fishel-722a72165/" >
              <i class="fab fa-linkedin"></i>
              </a>
            </span>
          </div>
        </div>


        <div class="column"> 
            <p>
            <i class="far fa-copyright"></i> 
            {{getDate()}}
            Nathaniel Fishel
            </p>
          
          
        </div>

      </div>
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
        { hid: 'description', name: 'description', content: 'My custom description' }
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