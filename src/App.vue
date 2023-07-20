<script setup>
import { ref } from '@vue/reactivity';

import newcomp from './components/newcomp.vue';
import HelloWorld from './components/HelloWorld.vue'
let level2 = ref(false) 
const nextLevel =()=>{
  level2.value=!level2.value;
}

</script>

<template>
  <header>
     <div>
         <newcomp @toggleTow="nextLevel" v-show="!level2"/>
         <HelloWorld @back="nextLevel" v-show="level2"/>
</div>      
  </header>

</template>

<style scoped>
header {
  line-height: 1.5;
  display: flex; /* נוסף */
  flex-direction: column; /* נוסף */
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
