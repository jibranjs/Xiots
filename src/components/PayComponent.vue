<template>
    <section>
        <form class="flex flex-col gap-2 !pt-5 !pb-12">
            <label class="font-bold !mx-[50px]">Name</label>
            <InputText type="Text" required placeholder="Enter Your Name" class="!bg-white !text-black !mx-12" />
            <label class="font-bold !mx-[50px]">Card Number</label>
            <InputText type="email" required placeholder="Email Address" class="!bg-white !text-black !mx-12" />
            <label class="font-bold !mx-[50px]">Date</label>
            <DatePicker v-model="value2" placeholder="MM / DD / YY" showIcon iconDisplay="input" class="!mx-12 !w-[250px]" />
            <label class="font-bold !mx-[50px] ">CVV</label>
            <InputText type="number" required placeholder="Cvv" class="!bg-white !text-black !mx-12" />           
          
        </form>
    </section>
</template>
<script setup>
import DatePicker from 'primevue/datepicker';
import InputText from 'primevue/inputtext';


</script>