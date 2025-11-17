<template>
    <form class="flex flex-col gap-2 !pt-5 !pb-12">
        <label class="font-bold !mx-[50px]">Name</label>
        <InputText type="Text" required placeholder="Enter Your Name" class="!bg-white !text-black !mx-12" />
        <label class="font-bold !mx-[50px]">Email</label>
        <InputText type="email" required placeholder="Email Address" class="!bg-white !text-black !mx-12" />
        <label class="font-bold !mx-[50px]">Phone Number</label>
        <InputText type="number" required placeholder="Phone Number" class="!bg-white !text-black !mx-12" />
        <label class="font-bold !mx-[50px] ">Notes</label>
        <Textarea v-model="value" rows="5" cols="30" class="!mx-12 !bg-white !text-black" />
    </form>
</template>
<script setup>
import InputText from 'primevue/inputtext';
import Textarea from 'primevue/textarea';
</script>