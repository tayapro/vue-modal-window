<script setup>
const props = defineProps(['prop_visible'])
</script>

<template>
    <div v-if="prop_visible" class="overlay">
        <div class="center">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.overlay {
    background-color: rgba(99, 119, 119, 0.362);
    height: 100vh;
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 100;
}

.center {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}
</style>
