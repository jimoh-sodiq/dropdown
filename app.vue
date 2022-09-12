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

    <div class="flex justify-center">
  <div>
    <div class="dropdown relative">
      <button
        class="
          dropdown-toggle
          px-6
          py-2.5
          bg-blue-600
          text-white
          font-medium
          text-xs
          leading-tight
          uppercase
          rounded
          shadow-md
          hover:bg-blue-700 hover:shadow-lg
          focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0
          active:bg-blue-800 active:shadow-lg active:text-white
          transition
          duration-150
          ease-in-out
          flex
          items-center
          whitespace-nowrap
        "
        type="button"
        id="dropdownMenuButton1"
        data-bs-toggle="dropdown"
        aria-expanded="false"
      >
        Dropdown button
        <svg
          aria-hidden="true"
          focusable="false"
          data-prefix="fas"
          data-icon="caret-down"
          class="w-2 ml-2"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 320 512"
        >
          <path
            fill="currentColor"
            d="M31.3 192h257.3c17.8 0 26.7 21.5 14.1 34.1L174.1 354.8c-7.8 7.8-20.5 7.8-28.3 0L17.2 226.1C4.6 213.5 13.5 192 31.3 192z"
          ></path>
        </svg>
      </button>
      <ul
        class="
          dropdown-menu
          min-w-max
          absolute
          hidden
          bg-white
          text-base
          z-50
          float-left
          py-2
          list-none
          text-left
          rounded-lg
          shadow-lg
          mt-1
          m-0
          bg-clip-padding
          border-none
        "
        aria-labelledby="dropdownMenuButton1"
      >
        <li>
          <a
            class="
              dropdown-item
              text-sm
              py-2
              px-4
              font-normal
              block
              w-full
              whitespace-nowrap
              bg-transparent
              text-gray-700
              hover:bg-gray-100
            "
            href="#"
            >Action</a
          >
        </li>
        <li>
          <a
            class="
              dropdown-item
              text-sm
              py-2
              px-4
              font-normal
              block
              w-full
              whitespace-nowrap
              bg-transparent
              text-gray-700
              hover:bg-gray-100
            "
            href="#"
            >Another action</a
          >
        </li>
        <li>
          <a
            class="
              dropdown-item
              text-sm
              py-2
              px-4
              font-normal
              block
              w-full
              whitespace-nowrap
              bg-transparent
              text-gray-700
              hover:bg-gray-100
            "
            href="#"
            >Something else here</a
          >
        </li>
      </ul>
    </div>
  </div>
</div>
  </div>
</template>

<script>
  
</script>

// possible improvements

// use provide and inject instead of scoped slots for hiding more component logic from the user

