<template>
  <div class="h-screen flex flex-col items-center py-16">
    <!-- <NuxtWelcome /> -->
    <h1 class="mb-16">DropDown &#x1F973;</h1>
    <Menu v-slot="slotProps" class="relative inline-block text-left mb-16">
      <MenuButton
        @click="slotProps.toggle"
        class="inline-flex w-full justify-center rounded-md bg-purple-600 px-4 py-2 text-sm font-medium text-white hover:bg-opacity-80 focus:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-75"
      >
        Choose option
      </MenuButton>
      <transition
        enter-active-class="transition duration-100 ease-out"
        enter-from-class="transform scale-95 opacity-0"
        enter-to-class="transform scale-100 opacity-100"
        leave-active-class="transition duration-75 ease-in"
        leave-from-class="transform scale-100 opacity-100"
        leave-to-class="transform scale-95 opacity-0"
      >
        <MenuItems
          v-if="slotProps.isOpen"
          class="absolute right-0 mt-2 w-56 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none z-30"
        >
          <MenuItem
            class="group flex w-full items-center rounded-md px-2 py-2 text-sm cursor-pointer"
          >
            Account settings
          </MenuItem>
          <MenuItem
            class="group flex w-full items-center rounded-md px-2 py-2 text-sm cursor-pointer"
          >
            Support
          </MenuItem>
          <MenuItem
            class="group flex w-full items-center rounded-md px-2 py-2 text-sm cursor-pointer"
          >
            License 
          </MenuItem>
          <MenuItem
            class="group flex w-full items-center rounded-md px-2 py-2 text-sm cursor-pointer"
          >
            Sign out
          </MenuItem>
        </MenuItems>
      </transition>
    </Menu>
    <h1>Testing overlay of the dropdown</h1>
  </div>
</template>

<script>
  
</script>

// possible improvements

// use provide and inject instead of scoped slots for hiding more component logic from the user