<template>
  <section>
   
   <section>
      <div class="columns">
        <div  class="column main-text">
          <h1>Nathaniel Fishel</h1>
          <b-button tag="router-link" :to="{ path: '/portfolio' }" class="button is-medium is-link">View my work</b-button>
          <b-button tag="router-link" :to="{ path: '/about' }" class="button is-medium is-dark">Read my résumé</b-button>
        </div>

        
        <div class="column">
            <!-- <img class="circle-pic" src="~/assets/css/me.png" alt="a picture of me"> -->
        </div>
      </div>
   </section>

   <section>
      <div>
        <h2 class="main-body">
          Welcome to my personal website, here you can view my work or read more about me.
          this site is under constant develoment so check back soon!
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
   





  </section> 
</template>


<script>
export default {
  layout: "navbar",

head: {
  link:[{
    href: 'https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap', rel: "stylesheet"
  }]
}
}
</script>
