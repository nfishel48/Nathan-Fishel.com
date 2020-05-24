<template>
    <section>
        <h1 class="main-text" style=" padding-bottom: 1%;">Contact me</h1>
        <h2 class="main-body" style="font-size:150%; padding-left: 5%;">Please fill out the form below to reach me</h2>
  

        <div style="padding-left:10%; padding-right:10%;">
            <form name="contact" action="" method="post" netlify>
                <!-- Honey Pot -->
                <input type="hidden" name="form-name" value="contact" />

                <div style="padding-top: 2%;">
                    <label class="label"  for="name">Name</label>
                    <input  class="input" type="text" name="name" />
                </div>
                <div style="padding-top: 2%;">
                    <label  class="label"  for="email">Email</label>
                    <input  class="input" type="email" name="email"  />
                </div>
                <div style="padding-top: 2%;">
                    <label   class="label" for="message">Message </label>
                    <textarea class="textarea is-medium"  name="message"></textarea>
                </div>
                <div style="padding-top: 5%;">
                    <input class="button is-success" type="submit" value="Submit">
                </div>
            </form>
        </div>


        <div style="padding: 100px;">
        </div>

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