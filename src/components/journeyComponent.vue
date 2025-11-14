<template>
    <StepPanel v-slot="{ activateCallback }" value="1">
    <form sb class="flex flex-col py-12">
       <label class="font-bold !mx-[50px] !mb-1">PICKUP LOCATION</label>
            <InputText type="Text" v-model="value" placeholder="Pick Up Location" class="!bg-white !text-black !mb-4 !mx-12" />
       <label class="font-bold !mx-[50px] !mb-1">DROP OFF LOCATION</label>
            <InputText type="Text" required="" placeholder="Pick Up Location" class="!bg-white !text-black !mx-12" />
        <div class="!mx-12 !mt-3 flex justify-end">
            <Button label="Next" @click="activateCallback('2')" severity="info" class="!text-white !px-6 !py-2 !mb-3" />
        </div>
    </form>
    </StepPanel>
</template>
<script setup>

import StepPanel from 'primevue/steppanel';
import InputText  from 'primevue/inputtext';
import Button from 'primevue/button';
</script>