<script setup>
import Button from 'primevue/button';
import Stepper from 'primevue/stepper';
import StepList from 'primevue/steplist';
import StepPanels from 'primevue/steppanels';
import StepItem from 'primevue/stepitem';
import Step from 'primevue/step';
import StepPanel from 'primevue/steppanel';
import { ref } from 'vue';
import JourneyComponent from '@/components/journeyComponent.vue';
import VechileComponent from '@/components/VechileComponent.vue';
import InfoComponents from '@/components/infoComponents.vue';
import PayComponent from '@/components/PayComponent.vue';

const value = ref()
</script>
<template>
    <section class="bg-[#FFC0F9]">
        <div class="!max-w-[1536px] !mx-auto !py-12 lg:py-8">
            <h2 class="text- !font-bold">Book Your Journey</h2>
            <div class="card flex justify-center">
                <Stepper value="1" class="basis-[50rem]">
                    <StepList>
                        <Step value="1">Journey</Step>
                        <Step value="2">Vechile</Step>
                        <Step value="3">Info</Step>
                        <Step value="4">Pay</Step>
                    </StepList>
                    <StepPanels>
                        <StepPanel v-slot="{ activateCallback }" value="1">
                            <JourneyComponent />
                            <div class="!mx-12 flex justify-end">
                                <Button label="Next" @click="activateCallback('2')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                            </div>
                        </StepPanel>
                        <StepPanel v-slot="{ activateCallback }" value="2">
                            <VechileComponent />
                            <div class="!mx-12 flex justify-between">
                                <Button label="Back" @click="activateCallback('1')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                                <Button label="Next" @click="activateCallback('3')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                            </div>
                        </StepPanel>
                        <StepPanel v-slot="{ activateCallback }" value="3">
                            <InfoComponents />
                            <div class="!mx-12 flex justify-between">
                                <Button label="Back" @click="activateCallback('2')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                                <Button label="Next" @click="activateCallback('4')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                            </div>
                        </StepPanel>
                        <StepPanel v-slot="{ activateCallback }" value="4">
                            <PayComponent />
                            <div class="!mx-12 flex justify-between">
                                <Button label="Back" @click="activateCallback('3')" severity="info"
                                    class="!text-white !px-6 !mb-3" />
                                <Button label="Submit" class="!text-white !px-6 !mb-3" />
                            </div>
                        </StepPanel>
                    </StepPanels>
                </Stepper>
            </div>
        </div>
    </section>

</template>
