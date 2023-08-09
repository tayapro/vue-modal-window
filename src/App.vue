<script setup>
import { ref } from 'vue'
import ConfirmationModal from './components/ConfirmationModal.vue'
import LoginModal from './components/LoginModal.vue'

let modals = ref({
    confirm: false,
    login: false,
})
</script>

<template>
    <button @click="modals.confirm = true">Are you ok?</button>
    <button @click="modals.login = true">Login</button>
    <ConfirmationModal
        :prop_visible="modals.confirm"
        prop_title="Are you sure?"
        @deny="modals.confirm = false"
        @confirm="modals.confirm = false"
    />
    <LoginModal
        :prop_visible="modals.login"
        @cancel="modals.login = false"
        @submit="modals.login = false"
    />
</template>

<style scoped></style>
