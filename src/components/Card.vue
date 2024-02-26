
<template>
  <div class="card w-full max-w-[1162px] mx-auto">
    <div class="card-header pb-10 border-b border-gray-300 ">
      <h1 class="font-bold text-2xl">User Registration Form</h1>
    </div>
    <div class="card-body grid grid-cols-1 gap-6 mt-10">
      <div>
        <InputForm
            type='text'
            label="Full Name as per Aadhaar"
            isRequired={true}
            labelClass="text-[0.75rem] font-medium"
            placeholder="Enter full name as per Aadhaar"
        />
      </div>

      <div>
        <InputForm type='text'
                   label="Mobile Number as per Aadhaar"
                   isRequired={true}
                   placeholder="Enter Mobile Number as per Aadhaar"
                   buttonLabel="Generate OTP"
                   labelClass="text-[0.75rem] font-medium"
        />
      </div>

      <div>
        <InputForm type='text'
                   label="An OTP has been sent to your registered mobile numberXXXXXX5676"
                   placeholder="Enter Mobile Number as per Aadhaar"
                   buttonLabel="Verify OTP"
                   labelClass="text-[0.75rem] font-medium text-sky-500"
                   disable={true}
        />
        <div class="text-[0.75rem] font-medium mt-2">
          Don't receive the OTP ? <span class="text-orange-500">RESEND OTP</span>
        </div>
      </div>

      <div>
        <InputForm type='email'
                   label="Personal Email ID"
                   isRequired={true}
                   placeholder="Enter Mobile Number as per Aadhaar"
                   buttonLabel="Generate OTP"
                   labelClass="text-[0.75rem] font-medium"
        />
      </div>

      <div>
        <InputForm type='text'
                   label="An OTP has been sent to your Personal Email ID"
                   placeholder="Enter Mobile Number as per Aadhaar"
                   buttonLabel="Verify OTP"
                   labelClass="text-[0.75rem] font-medium text-sky-500"
                   disable={true}
        />
        <div class="text-[0.75rem] font-medium mt-2">
          Don't receive the OTP ? <span class="text-orange-500">RESEND OTP</span>
        </div>
      </div>


      <div>
        <InputForm type='text'
                   label="Aadhaar Number (for eKYC Verfication)"
                   isRequired={true}
                   placeholder="Enter Mobile Number as per Aadhaar"
                   buttonLabel="eKYC"
                   labelClass="text-[0.75rem] font-medium"
        />
        <div class="text-[0.75rem] text-gray-400 mt-2">
          12 Digit UUID(1234/1234/1234)
        </div>
      </div>

    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-10">
      <div class="flex flex-col">
        <p class="text-[0.75rem] font-medium mt-2">Are you Human?</p>
        <div class="flex flex-row gap-2 justify-start items-center">
          <div class="w-[80%] h-auto" >
            <img src="/images/screenshot-20240201-122023-1@2x.png">
          </div>
          <div class="w-[50px] h-auto">
            <img  src="/images/oirefresh.svg"/>
          </div>


        </div>
        <div class="text-[0.75rem] text-gray-400 mt-2">
          Unable to Read ? <span class="text-sky-500 underline">Try Another</span>
        </div>
      </div>
      <div class="items-center my-auto">
        <input class=" border border-gray-400 rounded py-2 px-3 w-full max-w-[460px]"  placeholder="Enter the answer" value=""/>
      </div>
    </div>
    <div class="flex justify-center mt-10">
      <div>
        <button class="bg-orange-500 px-12 py-3 text-white text-xl rounded-lg">Submit</button>
      </div>
    </div>
  </div>
</template>
<script setup>
import InputForm from "@/components/InputForm.vue";
</script>
<style lang="scss">
.card {
  @apply bg-[#faf8f8] p-16 rounded-xl my-8;

  &-header{
    @apply my-5;
  }
}
</style>