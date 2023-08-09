<script setup>
import ModalBase from './lib/ModalBase.vue'
const emit = defineEmits(['deny', 'confirm'])
const props = defineProps(['prop_title'])
</script>

<template>
    <ModalBase>
        <div class="modal">
            <h1>{{ props.prop_title }}</h1>
            <button @click="emit('confirm')">Yes</button>
            <button @click="emit('deny')">No</button>
        </div>
    </ModalBase>
</template>

<style scoped>
.modal {
    background-color: rgb(255, 255, 255);
    padding: 2rem;
    box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.35);
}
</style>
