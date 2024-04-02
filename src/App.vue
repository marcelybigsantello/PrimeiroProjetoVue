<script setup>

import { ref } from 'vue';
import LoginPage from './components/LoginPage.vue';
import PageNotFound from './components/PageNotFound.vue';

const routes = {
  '/': LoginPage,
  '': LoginPage
};

const errors = ref({
  email:[],
  password: []
})

const onSubmit = async() => {
  Object.assign(errors.value, {email: [], password: []});

  if (/\w+@\w+\.\w+/.test(email.length)){
    return 'Email incorreto. Informe novamente o seu email';
  }

  if (password.length == 0 ){
    return 'Informe a sua senha';
  }

}

const currentPath = ref(window.location.hash);
window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash;
})

const currentView = computed(() =>{
  return routes[currentPath.value.slice(1)] || PageNotFound;

});

await fetch ('/submit', {
  method: 'POST',
  headers: {
    'content-type': 'application/json'
  },
  body: JSON.stringify({ email: email.value, password: password.value })
})

</script>
<template>
  <h1>Página Inicial</h1>
</template>
<style></style>
