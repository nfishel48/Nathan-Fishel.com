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
        </nav>
        
        <nav class="level">
        <div class="level-item has-text-centered">
         <div v-for="(projects, index) in projectTwo" :key="index">
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
        </nav>
        
        <div style="padding-bottom: 200px;"
    ></div>
    </section>
    
</template>
<script>

export default {
    layout: 'navbar',

  data () {
    return {
      project: [
        {title: 'My website', img: '/website.png', link: 'https://nathanfishel.com/', code: 'https://github.com/nfishel48/Personal-site'},
        {title: 'Simntx', img: '/simntx.png',  link: 'https://simntx.herokuapp.com/', code: 'Closed Source'},
        {title: 'Coming soon', img: '/logo.jpg',  link: '#', code: '#'},
      ],
      projectTwo: [
        {title: 'Coming soon', img: '/logo.jpg',  link: '#', code: '#'},
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