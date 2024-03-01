<script setup>

</script>

<template>
  <div class="main-menu ">
    <div class="flex flex-row justify-start items-center gap-4 mx-auto">
      <div>
        <img src="/images/digitalindia-1.svg">
      </div>
      <div>
        <img src="/images/akam-1.svg">
      </div>
      <div class="w-[187px]">
        <img src="/images/frame-44454@2x.png">
      </div>
    </div>

    <div class="flex flex-row gap-6 items-center text-gray-600 mx-auto">
      <div class="flex flex-row gap-1"><div><img src="/images/vector.svg"/></div>Help</div>
      <div>Contact Us</div>
      <div>FAQ</div>
      <button class="menu-button">SSO Login</button>
      <button class="menu-button">Register</button>
    </div>
  </div>
</template>

<style lang="scss">

.main-menu{
  @apply flex flex-col lg:flex-row gap-3 justify-center lg:justify-between py-3 container mt-2 max-w-full relative;
  &::after{
    position: absolute;
    content: " ";
    width: 90%;
    @apply bg-gray-600;
    height: 1px;
    bottom: 0;
  }
}

.menu-button {
  @apply hover:bg-orange-500 hover:text-white text-orange-500 border border-orange-500 rounded-2xl px-6 py-1;
}
</style>