<template>
  <div>
    <label :class='labelClass'>{{ label }}
     <span v-if="isRequired" class="text-red-500">*</span>
    </label>
    <div class="flex flex-row gap-6 w-full mt-1">
      <input class=" border border-gray-400 rounded py-2 px-3 flex-grow max-w-[860px]"  :disabled='disable' :type='type' :placeholder='placeholder' value=""/>
      <template v-if="buttonLabel">

        <button class="flex-shrink border border-orange-500 hover:bg-orange-500 hover:text-white bg-orange-100 text-nowrap px-3 rounded-lg font-semibold min-w-[16ch]">
          {{ buttonLabel }}
        </button>
      </template>
    </div>
  </div>
</template>
<script setup>
defineProps(['type', 'placeholder', 'label', 'isRequired', 'buttonLabel', 'labelClass', 'disable'])
</script>
<style>

</style>