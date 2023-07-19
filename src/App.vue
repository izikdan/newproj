<script setup>
import { ref } from '@vue/reactivity';

import newcomp from './components/newcomp.vue';

</script>

<template>
  <header>
    <div>
         <newcomp msg="hello you her? where are you? where are you go?"/>
        
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
