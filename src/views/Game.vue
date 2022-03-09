<template>
  <h1>Estamos en el juego</h1>
  <p>{{ $route.params.name }}</p>
  <hr>


  <button @click="load">Cargar</button>
</template>

<script>
import { useRoute,useRouter } from "vue-router";

export default {
  setup() {
    const route = useRoute();
    const router = useRouter();

    // console.log(route.params);
    console.log(router);

    const load = () => {
       console.log('Ejecutando la petecion');

       setTimeout(() =>{
           console.log('volver a la home');
           router.push('/');//redige a la home
       },3000)
    }

    return{
        load,
    };
  },
};
</script>

<style></style>
