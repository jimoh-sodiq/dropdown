<template>
    <div>
        <slot :open="open" :close="close" :toggle="toggle" :is-open="isOpen" />
    </div>
</template>

<script setup>
    const isOpen = ref(false);
    const open =  () => {
        isOpen.value = true;
    }

    const close = () => {
        isOpen.value = false;
    }

    const toggle = () => {
        isOpen.value = !isOpen.value;
    }
</script>
