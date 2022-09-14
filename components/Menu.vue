<template>
    <div>
        <slot></slot>
        <!-- <slot :openDropdown="openDropdown" :closeDropdown="closeDropdown" :toggleDropconst toggleDropdown="toggleDropconst toggleDropdown" :is-openDropdown="dropdownIsOpen" /> -->
    </div>
</template>

<script setup>
    const dropdownIsOpen = ref(false);
    const openDropdown =  () => {
        dropdownIsOpen.value = true;
    }

    const closeDropdown = () => {
        dropdownIsOpen.value = false;
    }

    const toggleDropdown = () => {
        dropdownIsOpen.value = !dropdownIsOpen.value;
    }

    provide('dropdown', {
        dropdownIsOpen, closeDropdown, toggleDropdown, openDropdown
    })
</script>
