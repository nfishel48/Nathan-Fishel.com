<template>
  <section class="section" style="padding:0px;">
    
    <!-- Front page photo-->
      <section class="hero bg-img  is-fullheight">
    <!-- Hero head: will stick at the top -->
    <div id="hhead" class="hero-head">
      <header class="navbar">
        <div class="container">
          <div class="navbar-brand">
          <h1>Nathaniel Fishel</h1>
          <!--
            <a class="navbar-item">
              <img src="https://bulma.io/images/bulma-type-white.png" alt="Logo">
            </a>
            -->
            <span class="navbar-burger burger" data-target="navbarMenuHeroC">
              <span></span>
              <span></span>
              <span></span>
            </span>
          </div>
          <div id="navbarMenuHeroC" class="navbar-menu">
            <div class="navbar-end">
              <a class="navbar-item is-active" href="home">
                Home
              </a>
              <a class="navbar-item">
                About me
              </a>
              <a class="navbar-item">
                Portfolio
              </a>
              <span class="navbar-item">
                <a class="button is-link is-inverted">
                  <span>Contact me</span>
                </a>
              </span>
            </div>
          </div>
        </div>
      </header>
    </div>

    <!-- Hero content: will be in the middle -->
    <div class="hero-body">
      <div class="container has-text-centered">
        <div class=main-text>
          <h1 id="text" class="title" >
            You have reached Nathaniel Fishel's Portfolio!
          </h1>
        </div>
        
        <h2 class="subtitle">
            <button class="button is-large is-link">Click here to continue</button>
        </h2>
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
