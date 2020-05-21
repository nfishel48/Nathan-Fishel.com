<template>
    <section>
        <h1 class="main-text" style=" padding-bottom: 1%;">Contact me</h1>
        <h2 class="main-body" style="font-size:150%; padding-left: 5%;">Please fill out the form below to reach me</h2>
  
        
        <form name="ask-question" action="" method="post" netlify>
           
                    <input type="hidden" name="form-name" value="ask-question" />
                    <p>
                         <b-field label="Name" class="main-body" style="font-size:150%; padding-left: 5%;">
                            <b-input v-model="name"></b-input>
                        </b-field>
                    </p>
                    <p>
                        <b-field label="Email" class="main-body" style="font-size:150%; padding-left: 5%;">
                            <b-input v-model="email" type="email"></b-input>
                        </b-field>
                    </p>
                    <p>
                        <b-field label="Message" class="main-body" style="font-size:150%; padding-left: 5%;">
                            <b-input maxlength="200" type="textarea" v-model="message"></b-input>
                        </b-field>
                    </p>
        <div style="font-size:150%; padding-left: 5%;">
            <b-button  type="is-success" outlined>Submit</b-button>
        </div>
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