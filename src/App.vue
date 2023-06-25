<script setup>
import { ref } from 'vue';

import newcomp from './components/newcomp.vue';
// import NewComponent from './components/NewComponent.vue';

// let componentsData = ref([]);

// const addNewComponent = () => {
//   const componentName = 'NewComponent'; // שם הקומפוננטה החדשה
//   const msg = 'Hello World'; // הודעת הקומפוננטה החדשה
//   const componentData = {
//     component: componentName,
//     msg: msg,
//   };
//   componentsData.value.push(componentData);
// }
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <div>
         <newcomp msg="hello you her? where are you? where are you go?"/>
         <!-- <div>
      <component
        v-for="(componentData, index) in componentsData"
        :key="index"
        :is="componentData.component"
        :msg="componentData.msg"
      ></component>
    </div>
    <button @click="addNewComponent">הוסף קומפוננטה חדשה</button> -->

    <!-- <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="10" height="10" /> -->
</div>
    <!-- <div class="wrapper">
      <HelloWorld msg="hello world" />
    </div> -->
    
  </header>

  <!-- <main>
    <TheWelcome />
  </main> -->
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
