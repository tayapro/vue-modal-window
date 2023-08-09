<script setup>
import ModalBase from './lib/ModalBase.vue'
const emit = defineEmits(['cancel', 'submit'])
</script>

<template>
    <ModalBase>
        <div class="modal">
            <input type="text" placeholder="username" />
            <input type="text" placeholder="password" />
            <button @click="emit('submit')">submit</button>
            <button @click="emit('cancel')">cancel</button>
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
