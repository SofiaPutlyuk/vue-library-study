<template>
    <div class="container-card">
        <img :src="imgAvatar" :alt="title" class="image" />
        <p>Ім'я: {{ name }}</p>
        <p>Вік: {{ age }}</p>
        <p>Місто : {{ city }}</p>
        <ul class="container-list">
            Хоббі:
            <li v-for="(description, index) in description" :key="index" class="list">
                {{ description }}
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    props: {
        name: String,
        age: Number,
        imgAvatar: String,
        title: String,
        city: String,
        description: Array
    }
}
</script>
<style>
.container-card {
    width: 300px;
    height: 400px;
    border-radius: 20px;
    background-color: rgb(255, 207, 135);
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.image {
    width: 200px;
    margin-top: 30px;
    border-radius: 20px;
}

.list {
    list-style: none;
    color:rgb(200, 86, 86)
}
.container-list {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap:10px;
}
</style>