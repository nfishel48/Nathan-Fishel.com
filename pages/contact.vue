<template>
    <section>
        <h1 class="main-text" style=" padding-bottom: 1%;">Contact me</h1>
        <h2 class="main-body" style="font-size:150%; padding-left: 5%;">Please fill out the form below to reach me</h2>
        <form id="contact-form" name="contact" netlify>
            <b-field label="Name">
                <b-input v-model="name"
                type="text"
                required
              ></b-input>
            </b-field>
            
            <b-field  label="Email"
                >
                <b-input 
                    type="email"
                    required
                    maxlength="30">
                </b-input>
            </b-field>
            
            <b-field  label="Message">
                <b-input maxlength="200" type="textarea"
                required
                ></b-input>
            </b-field>

            <b-button type="is-success" outlined>Submit</b-button>
        </form>
    </section>
</template>

<script>
export default {
    layout: 'navbar'
    
}
</script>