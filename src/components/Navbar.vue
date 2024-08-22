<script setup>

const getData = async () => {
    const req = await fetch("https://jsonplaceholder.typicode.com/posts")
    const res = await req.json()
}

getData()

</script>

<template>
   <div v-for="item in res" :key="item.id">
    <h1>{{ item.title }}</h1>
    <h2>{{ item.userId }}</h2>
    <p>{{ item.body }}</p>
   </div>
</template>

<style>
h1 {
    color: rgb(3, 11, 22);
    text-transform: uppercase;
}

h2 {
    text-transform: capitalize;
}

p{
    font-size: larger;
}

.blog {
    background-color: rgba(128, 128, 128, 0.274);
    padding: 1rem;
    margin: 1rem;
    font-family: 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    transition: 0.4s
}

.blog:hover{
    background-color: rgb(155, 155, 155);
    cursor: pointer;
    transition: 0.4s
}
</style>