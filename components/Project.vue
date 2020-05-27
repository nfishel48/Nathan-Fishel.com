<template>
<section>
<script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
   
    <div class="box" >
        <img  class="image is-128x128" src:{{img}} alt="Image">
            <p class="subtitle">{{title}}</p>
            <b-button>
              <a href="https://nathanfishel.com/">
              <i class="fas fa-code"></i>
                View Project
              </a>
            </b-button>
            <b-button  >
              <a href= 'https://github.com/nfishel48/Personal-site'>
              <i class="fab fa-github"></i>
                View Code
              </a>
            </b-button>
    </div>
  
</section>
</template>

<script>
export default {
  name: 'projects',
  props: {
      title: String,
      img: String
  }
}

</script>