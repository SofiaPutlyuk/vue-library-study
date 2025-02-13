<template>
  <div class="container">
    <h1>{{ message }}</h1>

    <img :src="imageUrl" class="image">

    <input v-model="name" placeholder="Введіть ім'я">
    <p>Введене ім'я: {{ name }}</p>

    <p v-if="isVisible">Цей текст видно</p>
    <button @click="isVisible = !isVisible">Перемкнути</button>

    <input v-model="newItem" placeholder="Нова справа">
    <button @click="addItem">Додати</button>

    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Привіт, Vue!",
      imageUrl: "https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_3x2.jpg",
      name: "",
      isVisible: true,
      items: [],
      newItem: ""
    };
  },
  methods: {
    addItem() {
      if (this.newItem.trim() !== "") {
        this.items.push(this.newItem);
        this.newItem = "";
      }
    }
  }
};
</script>

<style>
.image {
  width: 100px;
  height: 100px;
}

.container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
</style>
