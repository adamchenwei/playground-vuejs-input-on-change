<template>
  <form action="http://localhost:8080" method="post" autocomplete="on">
    <input required type="email" @input="onChange" @blur="onBlur" name="email" id="email" autocomplete="username email" />
    <input required type="password" @input="onChange" @blur="onBlur" name="password" id="password" autocomplete="password new-password"/>
    <button type="submit">Submit</button>
  </form>
  <!-- <form action="http://localhost:8080" method="post" target="registerframe">
    <label>Username :</label>
    <input type="text" name="username" id="username" />
    <label>Password :</label>
    <input type="password" name="password" id="password"/>
    <br/>
    <button type="submit" id="register" name="register">register!</button>
  </form> -->
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      console.log('onsubmit');
      console.log(event);
      window.location.href = 'http://localhost:8081/?abc=loggedin'
    },
    onBlur(event) {
      console.log(event);
    },
    onChange(event) {
      console.log(event);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
