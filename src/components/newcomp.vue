

<template>
  <div class="greetings">
     <h1 class="green">{{ msg }}</h1>
    <!-- <h1>{{ user }}</h1> -->
    <!-- <button @click="chengName">שנה שם</button> -->
  </div>
  <div>
    <h1>יומן</h1>
    <button @click="toggleCalendar" >פתח לוח שנה</button>
    <div v-if="showCalendar">
      <input type="datetime-local" v-model="selectedDate">
      <button @click="toggleCalendar2">בחר</button>
    </div>
    <div v-if="putName">
      <input type="text" v-model="name">שם
      <button @click="toggleCalendar3">סיים</button>
    </div>
    <div v-if="users.length > 0">
      <h1 >פגישות שמורות</h1>
      <ul>
        <li v-for="(user, index) in users" :key="index" @click="">
          <a @click="toggleCalendar4">תאריך: {{ user.selectedDate }} :שם: {{ user.name }}</a>
        </li>
      </ul>
    </div>
    <div v-if= "details">
      <textarea name="addDetails" id="addDetails" cols="30" rows="10">       פרטים נוספים</textarea>
    </div>
  </div>
</template>

<script setup>
import { ref } from '@vue/reactivity';

let showCalendar = ref(false);
let putName = ref(false);
let selectedDate = ref("");
let name = ref("");
let user = ref("")
let users = ref([]);
let details = ref(false)

const toggleCalendar = () => {
  showCalendar.value = !showCalendar.value;

}
const toggleCalendar2 = () => {
  putName.value = !putName.value;

}
const toggleCalendar3 = () => {
  toggleCalendar();
  toggleCalendar2();
  const user = { selectedDate: selectedDate.value, name: name.value }
  users.value.push(user)
  selectedDate.value = "";
  name.value = ""
}
const toggleCalendar4 =()=>{
  details.value=!details.value;
}
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>
<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
  color: aquamarine;
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
