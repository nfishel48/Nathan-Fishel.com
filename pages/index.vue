<template>
  <section class="section" style="padding:0px;">
    
    <!-- Front page photo-->
      <section class="hero bg-img  is-fullheight">
    <!-- Hero head: will stick at the top -->
    <div id="hhead" class="hero-head">
    </div>

    <!-- Hero content: will be in the middle -->
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class="main-text">
          <h1 id="text" class="title">
            You have reached Nathaniel Fishel's Portfolio!
          </h1>
        </div>
        
        <a class="subtitle">
            <b-button tag="router-link" :to="{ path: '/home' }" class="button is-large is-link">Click here to continue</b-button>
        </a>
      </div>
    </div>

    <!-- Hero footer: will stick at the bottom -->
    <div class="hero-foot">
      <nav class="tabs is-boxed is-fullwidth">
        <div class="container">
          <!-- bottom tabs-->
        </div>
      </nav>
    </div>
 </section>
 </section>

    <!-- Below this is outside of image -->

</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',
  layout: 'nofooter',

  
  methods: {
    say: function (message) {
      alert(message)
    }
  },
  components: {
    Card
  },
   head: {
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
}
}


</script>
