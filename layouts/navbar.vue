

<template>
  <div id ="content">
    <div id="main-nav">
      <b-navbar>
          <template slot="brand">
              <b-navbar-item tag="router-link" :to="{ path: '/' }">
              <h3>Nathaniel Fishel</h3>
                  <!--
                  <img
                      src="https://raw.githubusercontent.com/buefy/buefy/dev/static/img/buefy-logo.png"
                      alt="Lightweight UI components for Vue.js based on Bulma"
                  >
                  -->
              </b-navbar-item>
          </template>
          <template slot="start">
              <b-navbar-item tag="a" href="#">
                  Home
              </b-navbar-item>
              <b-navbar-item href="#">
                  Portflolio
              </b-navbar-item>
              <b-navbar-dropdown label="Info">
                  <b-navbar-item href="#">
                      About
                  </b-navbar-item>
                  <b-navbar-item href="#">
                      Resume
                  </b-navbar-item>
                  <b-navbar-item href="#">
                      Contact
                  </b-navbar-item>
              </b-navbar-dropdown>
          </template>

          <template slot="end">
              <b-navbar-item tag="div">
                  <div class="buttons">
                      <a class="button is-primary">
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