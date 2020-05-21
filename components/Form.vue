<template>
  <form
    name="ask-question"
    method="post"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    >
    <input type="hidden" name="form-name" value="ask-question" />
    <p>
        <label for="name">Name:</label>
        <input id="name" v-model ="name">
    </p>
    <p>
        <label for="email">Email:</label>
        <input id="email" v-model ="email">
    </p>
    <p>
        <label for="message">Message:</label>
        <textarea id="message" v-model="message"></textarea>
    </p>

  </form>
</template>
<script>
export default {
  data () {
    return {
      name: null,
      email: null,
      message: null
    }
  }
}
</script>
