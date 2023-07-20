
<template>
 <textarea @click="$emit('back')" name="addDetails" id="addDetails" cols="30" rows="10" >       פרטים נוספים</textarea>
</template>


<script setup>

</script>
<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
