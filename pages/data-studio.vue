<template>
  <section>
   <script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
   <section>
      <div class="columns">
        <div  class="column main-text">
          <h1>Nathaniel Fishel</h1>
          <div id="buttons">
            <b-button tag="router-link" :to="{ path: '/portfolio' }" class="button is-medium is-link">View my work</b-button>
            <b-button tag="router-link" :to="{ path: '/about' }" class="button is-medium is-dark">Read my résumé</b-button>
          </div>
        </div>

        <div class="column main-text">
            <span id="github" class="icon">
              <a href="https://github.com/nfishel48">
              <i class="fab fa-github"></i>
              </a>
            </span>
            <span id="linkedin" style="padding-left: 10%;" class="icon">
              <a href="https://www.linkedin.com/in/nathaniel-fishel-722a72165/" >
              <i class="fab fa-linkedin"></i>
              </a>
            </span>
        </div>
      </div>
   </section>

   <section>
      <div id="body">
        <h2 class="main-body">
          <iframe width="600" height="450" src="https://datastudio.google.com/embed/reporting/305acc79-92fe-416d-9328-8bba27b2a01c/page/9C2UB" frameborder="0" style="border:0" allowfullscreen></iframe>
        </h2>
        <h2 class ="main-body">
          Currently planned features to this site incude a Professional Blog, and Photography gallery
        </h2>
          <div class="columns">
            <div class="column">

            </div>
            <div class="column">
             
            </div>
            <div class="column">
            </div>
          </div>
      </div>
   </section>
   
  <div style="padding-bottom: 100px;"></div>




  </section> 
</template>


<script>
export default {
  layout: "navbar",

head: {
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link:[{
    href: 'https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap', rel: "stylesheet"
  }]
},

}
</script>
