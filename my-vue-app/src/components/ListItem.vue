<template>
    <input type="text" v-model="searchItem" placeholder="Введіть завдання"/>
    <button @click="AddTasks">Додати</button>
    <ul>
      <li v-for="(task, index) in tasks" :key="index">{{ task }}</li>
    </ul>
</template>
<script setup>
import { ref , onUnmounted } from 'vue';
const tasks = ref([])
const searchItem = ref("")
const AddTasks = () => {
   if(searchItem.value.trim()){
    tasks.value.push(searchItem.value)
    searchItem.value = ""
   }
}
onUnmounted(() => {
alert("Компонент видалено!")
})
</script>