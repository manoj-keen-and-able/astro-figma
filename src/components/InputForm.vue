<template>
  <div>
    <label :class='labelClass'>{{ label }}
     <span v-if="isRequired" class="text-red-500">*</span>
    </label>
    <div class="flex flex-row gap-6 w-full mt-1">
      <input @input="dataChange" class=" border border-gray-400 rounded py-2 px-3 flex-grow max-w-[860px]"  :disabled='disable' :type='type' :placeholder='placeholder' v-model="internalValue"/>
      <template v-if="buttonLabel">

        <button @click="buttonClick" class="flex-shrink border border-orange-500 hover:bg-orange-500 hover:text-white bg-orange-100 text-nowrap px-3 rounded-lg font-semibold min-w-[16ch]">
          {{ buttonLabel }}
        </button>
      </template>
    </div>
    <div v-if="error" class="text-red-500 text-sm mt-1">{{ error }}</div>
  </div>
</template>
<script setup>

import {ref, watch} from "vue";

const emit = defineEmits(['update:value','button-click']);
const props = defineProps(['type', 'placeholder', 'label', 'isRequired', 'buttonLabel', 'labelClass', 'disable', 'value','dataChange','errorMessage'])

const internalValue = ref(props.value);

const dataChange = (event) => {
  internalValue.value = event.target.value;
  emit('update:value', internalValue.value); // Emit event to update value in parent
}
const buttonClick = () => {
  emit('button-click')
}

const error = ref(props.errorMessage);

watch(() => props.errorMessage, (newVal) => {
  error.value = newVal;
});

</script>
<style>

</style>