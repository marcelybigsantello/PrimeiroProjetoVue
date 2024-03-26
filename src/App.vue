<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <link rel="stylesheet" type="text/css" href="style.css" media="screen" />
    <img src="./images/github_logo.png" alt="Logo GitHub" width="60px" height="60px">
    <h1>Sign in to Github</h1>
  </header>
  <body>
    <form class="form-layout" name="form_login" method="POST" action="/tela_login">
      <div class="form-control">
        <label for="username" class="label">Username or email address</label>
        <input type="text" class="input" name="username" placeholder="" required>
      </div>
      <div class="form-control">
        <label for="password" class="label">Password</label>
        <input type="password" class="input" name="password" required>
        <a class="" href="/password_reset">Forgot password?</a>
      </div>
      <div>
        <input class="submit-button" type="button" name="commit" value="Sign in">
      </div>
    </form>
  </body>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
