<template>
    <section>
      <script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
        <h1 class="main-text">View some of my work</h1>
        <!--Level One-->
        <nav class="level">
        <div class="level-item has-text-centered">
         <div v-for="(projects, index) in project" :key="index">
           <div :id="'project'+index" class="box">
              <img  class="image is-128x128" :src='projects.img' alt="Image">
              <p class="subtitle">{{ projects.title }}</p>
              <b-button>
                <a :href='projects.link'>
                <i class="fas fa-code"></i>
                  View Project
                </a>
              </b-button>
              <b-button >
                <a :href="projects.code">
                <i class="fab fa-github"></i>
                  View Code
                </a>
              </b-button>
           </div>
          </div>
        </div>
        
        <!--Level two-->
        <!--
        <nav class="level">
        <div class="level-item has-text-centered">
            <div class="box">
            <img  class="image is-128x128" src="~/assets/css/logo.jpg" alt="placeholder">
            <p class="heading">Coming soon</p>
            <p class="content" style="color:white;">
                   "Lorem ipsum dolor sit amet, consectetur adipiscing elit,<br>
               eiusmod tempor incididunt ut labore et dolore magna aliq <br>
               ad minim veniam, quis nostrud exercitation ullamco labor <br>
               aliquip ex ea commodo consequat. Duis aute irure dolor i<br>
               in voluptate velit esse cillum dolore eu fugiat nulla p<br>
               sint occaecat cupidatat non proident, sunt in culpa qui o<br>
               "Lorem ipsum dolor sit amet, consectetur adipiscing eli<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in <br>
           
            </p>
            </div>
          </div>
          <div class="level-item has-text-centered">
            <div class="box">
            <img  class="image is-128x128" src="~/assets/css/logo.jpg" alt="placeholder">
            <p class="heading">Coming soon</p>
            <p class="content" style="color:white;">
               "Lorem ipsum dolor sit amet, consectetur adipiscing elit,<br>
               eiusmod tempor incididunt ut labore et dolore magna aliq <br>
               ad minim veniam, quis nostrud exercitation ullamco labor <br>
               aliquip ex ea commodo consequat. Duis aute irure dolor i<br>
               in voluptate velit esse cillum dolore eu fugiat nulla p<br>
               sint occaecat cupidatat non proident, sunt in culpa qui o<br>
               "Lorem ipsum dolor sit amet, consectetur adipiscing eli<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in <br>
           
            </p>
            </div>
          </div>
        <div class="level-item has-text-centered">
            <div class="box">
            <img  class="image is-128x128" src="~/assets/css/logo.jpg" alt="placeholder">
            <p class="heading">Coming soon</p>
            <p class="content" style="color:white;">
             "Lorem ipsum dolor sit amet, consectetur adipiscing elit,<br>
               eiusmod tempor incididunt ut labore et dolore magna aliq <br>
               ad minim veniam, quis nostrud exercitation ullamco labor <br>
               aliquip ex ea commodo consequat. Duis aute irure dolor i<br>
               in voluptate velit esse cillum dolore eu fugiat nulla p<br>
               sint occaecat cupidatat non proident, sunt in culpa qui o<br>
               "Lorem ipsum dolor sit amet, consectetur adipiscing eli<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in<br>
               aliquip ex ea commodo consequat. Duis aute irure dolor in <br>
            </p>
            </div>
        </div>
        -->
        </nav>
        
        <div style="padding-bottom: 200px;"
    ></div>
    </section>
    
</template>
<script>
import Project from '~/components/Project'
export default {
    layout: 'navbar',
    components: {
    Project
  },
  data () {
    return {
      project: [
        {title: 'My website', img: '/website.png', link: 'https://nathanfishel.com/', code: 'https://github.com/nfishel48/Personal-site'},
        {title: 'Coming soon', img: '/logo.jpg',  link: '#', code: '#'},
        {title: 'Coming soon', img: '/logo.jpg',  link: '#', code: '#'},
      ]      
    }
  },
  head: {
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
}

}
</script>