<template>
    <!-- Vechile -->
    <div v-for="vechile in vechiles" class="text-black !m-4"  @click="handleVehicle(vechile.slug)">
        <div :class="{'!bg-red-200': selectedVehicle===vechile.slug, 'bg-white p-4 cursor-pointer rounded-lg': true}">
            <div class="flex gap-6 justify-between items-center ">
                <div class="flex gap-8">
                    <img :src="vechile.image" :alt="vechile.name" class="w-[175px]">
                    <div>
                        <h2 class="text-xl font-bold">{{ vechile.name }}</h2>
                        <div class="text-sm flex gap-3">
                            <p>{{ vechile.persons}}</p>
                            <p>{{ vechile.luggage }}</p>
                        </div>
                    </div>
                </div>
                <h2 class="text-xl font-bold">{{ vechile.price }}</h2>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';


const selectedVehicle = ref('saloon')


const handleVehicle = (slug) => {
    selectedVehicle.value = slug
}

const vechiles = [
    {
        image:"/src/images/saloon.png",
        slug: "saloon",
        name:"Saloon Cars",
        persons:"4 Persons",
        luggage:"2 Luggage",
        price:"$18.00"
    },
    {
        image:"/src/images/estate.png",
        slug: "estate",
        name:"Estate",
        persons:"4 Persons",
        luggage:"2 Luggage",
        price:"$18.00"
    },
    {
        image:"/src/images/estate.png",
        slug: "comfort",
        name:"Comfort Car",
        persons:"4 Persons",
        luggage:"2 Luggage",
        price:"$18.00"
    },
    {
        image:"/src/images/mpv.png",
        slug: "6passengers",
        name:"6 Pessengers",
        persons:"6 Persons",
        luggage:"1 Luggage",
        price:"$26.70"
    },
       {
        image:"/src/images/minibus.png",
        slug: "8passengers",
        name:"8 Pessengers",
        persons:"8 Persons",
        luggage:"6 Luggage",
        price:"$26.10"
    }
]

</script>

<style>
.bg-danger{
    background-color: red;
}
</style>