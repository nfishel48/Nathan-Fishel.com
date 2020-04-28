

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
               <b-navbar-item class="nav-item"  tag="a" href="home">
                  Home
              </b-navbar-item>
              <b-navbar-item class="nav-item" href="about">
                  About Me
              </b-navbar-item>
              <b-navbar-item class="nav-item"  href="portfolio">
                  Portflolio
              </b-navbar-item>
              <b-navbar-item class="main-nav"  tag="div" >
                  <div class="buttons">
                      <a class="button button is-link is-inverted" href="contact">
                          <strong>Contact Me</strong>
                      </a>
                  </div>
              </b-navbar-item>
          </template>
      </b-navbar>
  </div>
  <nuxt/>
</div>   
</template>

<script>
export default {
      data () {
    return {
      title: 'Nathaniel Fishel'
      
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
}
</script>