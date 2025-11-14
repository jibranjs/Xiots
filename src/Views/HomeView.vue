<script setup>
import Button from 'primevue/button';
import Stepper from 'primevue/stepper';
import StepList from 'primevue/steplist';
import StepPanels from 'primevue/steppanels';
import StepItem from 'primevue/stepitem';
import Step from 'primevue/step';
import StepPanel from 'primevue/steppanel';
import InputText from 'primevue/inputtext';
import { ref } from 'vue';
import JourneyComponent from '@/components/journeyComponent.vue';

const value = ref()
</script>
<template>
    <div class="card flex justify-center">
        <Stepper value="1" class="basis-[50rem]">
            <StepList>
                <Step value="1">Journey</Step>
                <Step value="2">Vechile</Step>
                <Step value="3">Info</Step>
                <Step value="4">Pay</Step>
            </StepList>
            <StepPanels>

                <JourneyComponent />
        

            </StepPanels>
        </Stepper>
    </div>
</template>
