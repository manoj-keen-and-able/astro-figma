<script setup>
import Card from "@/components/Card.vue";
import TopBar from "@/components/shared/TopBar.vue";
import NavBar from "@/components/shared/NavBar.vue";
</script>

<template>
  <header>
    <TopBar/>
    <NavBar/>

  </header>
  <main>
    <div class="container mx-auto my-10">
      <ul class="breadcrumb">
        <li>HomeIcon</li>
        <li>FAQ</li>

      </ul>
    </div>
    <div class="container my-10">
      <!--      <Card/>-->
      <div class="w-full max-w-[1096px] mx-auto">
        <div class="my-5">
          <h1 class="text-[2.25rem] text-orange-500 font-bold">Frequently Ask Questions</h1>
        </div>
        <div>
          <p>Pellentesque cras adipiscing tempus libero vel nullam mauris tellus. Aliquam ultrices tellus consequat
            amet, lectus aliquam est in neque.</p>
          <!--          //Accordian-->
          <div class="mx-auto max-w-[854px] mt-4">
            <div class="collapse collapse-plus bg-white rounded-none border-b border-gray-300">
              <input type="radio" name="my-accordion-2" checked="checked"/>
              <div class="collapse-title text-[0.875rem] font-medium pl-10">
                Click to open this one and close others
              </div>
              <div class="collapse-content">
                <p>hello</p>
              </div>
            </div>
            <div class="collapse collapse-plus bg-white rounded-none border-b border-gray-300">
              <input type="radio" name="my-accordion-2"/>
              <div class="collapse-title text-[0.875rem] font-medium  pl-10">
                Click to open this one and close others
              </div>
              <div class="collapse-content">
                <p>hello</p>
              </div>
            </div>
            <div class="collapse collapse-plus bg-white rounded-none border-b border-gray-300">
              <input type="radio" name="my-accordion-2"/>
              <div class="collapse-title text-[0.875rem] font-medium pl-10">
                Click to open this one and close others
              </div>
              <div class="collapse-content">
                <p>hello</p>
              </div>
            </div>
          </div>
        </div>

      </div>

    </div>
    <div class="container">
        <div class="flex flex-row justify-between items-center gap-2">
          <div>
            Have any questions? <br/>
            Contact Us
          </div>

          <div class="flex flex-row justify-evenly items-start text-sm gap-2">

            <div class="flex flex-row items-start gap-2">
              <div>Phone Icon</div>
              <div class="flex flex-col">
                <div>Phone Number</div>
                <div>NIC Service Desk</div>
                <div class="font-bold">1800 111 555</div>
              </div>
            </div>

            <div class="flex flex-row items-start gap-2">
              <div>Email Icon</div>
              <div class="flex flex-col">
                <div>Email</div>
                <div>servicedesk@nic.in</div>
              </div>
            </div>

            <div class="flex flex-row items-start gap-2">
              <div>Email Icon</div>
              <div class="flex flex-col">
                <div>Email</div>
                <div>servicedesk@nic.in</div>
              </div>
            </div>

            <div class="flex flex-row items-start gap-2">
              <div>Email Icon</div>
              <div class="flex flex-col">
                <div>Email</div>
                <div>servicedesk@nic.in</div>
              </div>
            </div>

          </div>


        </div>
    </div>
  </main>
</template>

<style lang="scss">
.breadcrumb {
  @apply flex flex-row gap-3;
  > li {
    position: relative;

    &:nth-child(n+2) {
      &::before {
        position: absolute;
        content: "/";
        left: - 0.5rem;
      }
    }
  }
}
:root{
  @apply bg-gray-100;
}
.collapse-title{
  &:after{
    top:0.6rem !important;
    inset-inline-end: revert !important;
    inset-inline-start: 1rem !important;
    @apply text-blue-500 text-xl;
  }

}
.collapse-content{
  @apply ml-16 ;
  > p {
    @apply border-l-2 border-blue-500 pl-1;
  }
}
</style>
