<template>
  <section class="max-w-[1536px] mx-auto grid grid-cols-3 gap-4">
    <div v-for="product in products" :key="product.name" class="bg-[#ccc] rounded-lg !border">
      <img :src="product.image" :alt="product.name" class="w-[350px] mx-auto h-[450px] ">
      <div class="p-6 bg-white rounded-lg">
        <div class="flex justify-between !mb-3">
          <h2 class="text-black !font-bold text-2xl ">{{ product.name }}</h2>
          <Tag :severity="product.available">{{ product.stock }}</Tag>
        </div>
        <p class="text-black text-xl !mb-3 !font-bold">{{ product.price }}</p>
        <button class="bg-black py-2 px-4 rounded text-white w-full ">Add To cart</button>
      </div>
    </div>


  </section>

</template>
<script setup>
import Tag from 'primevue/tag';
const products = [
  {
    image: "/src/images/honor.avif",
    name: " Mobile Phone",
    price: "150$",
    stock: "In Stock",
    available: "success"

  },
  {
    image: "/src/images/heaphone.png",
    name: " Headphone",
    price: "100$",
    stock: "Limited",
    available: "warn"

  },
  {
    image: "/src/images/charger.png",
    name: "Charger",
    price: "15$",
    stock: "Out of stock",
    available: "danger"
  }

]

</script>
