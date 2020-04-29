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
            <b-button tag="a" href="./home" class="button is-large is-link">Click here to continue</b-button>
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
  
 

  //el:"#text",
  //mounted:function(){
    //this.method1() //method will exuctue on page load
  //},
  methods:{
    //Method to do type writer animation on Title
    // method1:function(){
    
    //   var i = 0;
    //   var txt = 'Lorem ipsum dummy text blabla.';
    //   var speed = 50; 
    //   for (i = 0; i < txt.length; i++) {    // make for loop to fix issue with the set timeout funcion
    //     document.getElementById("text").innerHTML += txt.charAt(i);
    //     console.log("working");
    //     setTimeout(this.method2(), 5000);
    //   }
    // },
  },


  components: {
    Card
  }
}


</script>
