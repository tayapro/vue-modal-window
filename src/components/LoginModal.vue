<script setup>
import { ref } from 'vue'
import ModalBase from './lib/ModalBase.vue'
const emit = defineEmits(['cancel', 'submit'])

const usernameRef = ref()
const passwordRef = ref()

function onSubmit() {
    const username = usernameRef.value.value
    const password = passwordRef.value.value
    emit('submit', username, password)
}
</script>

<template>
    <ModalBase>
        <div class="modal">
            <input ref="usernameRef" type="text" placeholder="username" />
            <input ref="passwordRef" type="text" placeholder="password" />
            <button @click="onSubmit()">submit</button>
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
