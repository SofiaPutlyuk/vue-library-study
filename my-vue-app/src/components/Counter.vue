<script setup>
import { ref , onMounted } from 'vue';
const count = ref(0)
const plusText = ref("Додати");
const minusText = ref("Відняти");
const AddNumber = () => {
    count.value++
    plusText.value = count.value % 2 === 0 ? "Додати" : "Збільшити";
}
const MinusNumber = () => {
    count.value--
    minusText.value = count.value % 2 === 0 ? "Відняти" : "Зменшити";
}
/*onMounted(() => {
alert("Компонент уже змонтовано!")
})*/
</script>
<template>
<p>{{count }}</p>
<button @click="AddNumber">{{ plusText }}</button>
<button @click="MinusNumber">{{ minusText }}</button>
</template>
