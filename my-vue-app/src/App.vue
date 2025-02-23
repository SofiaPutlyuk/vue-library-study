<script >
import UserProfile from './components/UserProfile.vue';
export default {
  components:{
   UserProfile
  }
}
</script>

<template>
<div>
<UserProfile 
name="Настя" 
:age=31
imgAvatar="https://unba.org.ua/assets/uploads/publications/publikacii/2020-12-09-prosyanyuk_5fd0a7453c136.jpg"
title="girl"
city="Kyiv"
:description="['Пише вірші','Читає','Малює']"
/>

 </div>
</template>



