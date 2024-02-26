<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <header>
    <div class="bg-slate-800 text-white w-full">
      <div class="flex flex-row justify-between container items-center">
        <div class="flex flex-row justify-start gap-2 items-center">
          <div class="w-auto h-[22px]">
            <img class="w-full h-full" src="/images/inidanflag@2x.png">
          </div>
          <div>
            Government of India
          </div>
        </div>
        <div>
          <ul class="right-menu text-sm">
            <li>Skip to Main Content</li>
            <li>A-</li>
            <li>A</li>
            <li>A+</li>
            <li><span><img src="/images/group-177.svg"></span></li>
            <li class="flex flex-row items-center"><span><img class="w-auto h-[20px]" src="/images/globe--20--regular.svg"></span>English</li>
          </ul>
        </div>
      </div>
    </div>
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
  </header>
  <main>
    <div class="container ">
      <Card/>
    </div>
  </main>
</template>

<style lang="scss">
.right-menu {
  @apply flex flex-row gap-1 items-center;
  > li:nth-child(n+2) {
    @apply relative;
    &::before {
      position: absolute;
      /*top: 0.2rem;*/
      left: -0.14rem;
      content: "";
      width: 1px;
      height: 1.2rem;
      @apply bg-gray-600;
    }
  }
  > li {
    @apply py-2 px-[1.5rem] cursor-pointer;
    &:hover{
      @apply bg-gray-500;
    }

  }
}

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
