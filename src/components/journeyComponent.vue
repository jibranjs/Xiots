<template>
    <form class="flex flex-col">
       <label class="font-bold !mx-[50px] !mb-1">PICKUP LOCATION</label>
            <InputText type="Text" required  placeholder="Pick Up Location" class="!bg-white !py-4 !text-black !mb-4 !mx-12" />
       <label class="font-bold !mx-[50px] !mb-1">DROP OFF LOCATION</label>
            <InputText type="Text" required placeholder="Pick Up Location" class="!bg-white !py-4 !text-black !mx-12" />
    </form>
</template>
<script setup>
import InputText  from 'primevue/inputtext';
</script>