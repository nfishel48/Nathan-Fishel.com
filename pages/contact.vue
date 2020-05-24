<template>
    <section>
        <h1 class="main-text" style=" padding-bottom: 1%;">Contact me</h1>
        <h2 class="main-body" style="font-size:150%; padding-left: 5%;">Please fill out the form below to reach me</h2>
  
    <form name="contact" netlify netlify-honeypot="bot-field" hidden>
        <label for="name">Name</label>
        <input type="text" name="name" />
        <label for="email">Email</label>
        <input type="email" name="email" />
        <label for="message">Message </label>
        <textarea name="message"></textarea>
    </form>


    </section>
</template>

<script>

export default {
    layout: 'navbar',
    components: {
    
  },
  data () {
    return {
      name: null,
      email: null,
      message: null
    }
  }
    
}

</script>