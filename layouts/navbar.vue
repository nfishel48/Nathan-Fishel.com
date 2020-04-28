

<template>
  <div id ="content">
    <div>
      <b-navbar class="main-nav">
          <template slot="brand">
              <b-navbar-item class="main-nav" tag="router-link" :to="{ path: '/' }">
              <h3>Nathaniel Fishel</h3>
                  <!--
                  <img
                      src="https://raw.githubusercontent.com/buefy/buefy/dev/static/img/buefy-logo.png"
                      alt="Lightweight UI components for Vue.js based on Bulma"
                  >
                  -->
              </b-navbar-item>
          </template>
          <template slot="start" class="main-nav">
             
          </template>

          <template slot="end" class="main-nav">
               <b-navbar-item class="nav-item"  tag="a" href="#">
                  Home
              </b-navbar-item>
              <b-navbar-item class="nav-item" href="#">
                  About Me
              </b-navbar-item>
              <b-navbar-item class="nav-item"  href="#">
                  Portflolio
              </b-navbar-item>
              <b-navbar-item class="main-nav"  tag="div">
                  <div class="buttons">
                      <a class="button button is-link is-inverted">
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