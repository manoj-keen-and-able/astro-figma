<script setup>

</script>

<template>
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
</template>

<style lang="scss" scoped>
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
</style>