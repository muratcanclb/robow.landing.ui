<script>
export default {
  methods: {
    isMobile() {
      if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true
      } else {
        return false
      }
    }
  }
}
</script>

<template>
  <div style="position: relative;">
    <header class="relative">
      <nav class="border-gray-200 px-4 lg:px-6 py-4 dark:bg-gray-800 relative z-50">
        <div class="grid grid-cols-3 items-center mx-auto max-w-screen-xl">
          <div class="flex justify-start items-center col-span-1">
            <button v-if="isMobile()"
              class="bg-primary-900 rounded-full text-sm md:text-base px-4 md:px-6 py-2 ml-2 focus:outline-none"
              style="background-color: white; border-width: 1px; font-size: 1rem;
        line-height: 1.5rem;  background-color: rgb(255 255 255 / var(--tw-bg-opacity));">Login</button>
          </div>
          <div class="flex items-center justify-center">
            <p v-if="!isMobile()" style="color: brown; font-size:60px; font-family:Georgia, serif,bold;">ROBOW</p>
            <p v-else style="color: brown; font-size:30px; font-family:Georgia, serif,bold;">ROBOW</p>
          </div>
          <div class="flex justify-end items-center col-span-1">
            <button v-if="!isMobile()"
              class="bg-primary-900 rounded-full text-sm md:text-base px-4 md:px-6 py-2 ml-2 focus:outline-none"
              style="background-color: white; border-width: 1px; ">Login</button>
            <button
              class="text-white bg-primary-900 rounded-full text-sm md:text-base px-4 md:px-6 py-2 ml-2 focus:outline-none"
              style="background-color: black;">Sign Up</button>
          </div>
        </div>
      </nav>
      <div class="max-w-xl mx-auto">
        <h1
          class="text-5xl font-extrabold leading-none tracking-tight text-primary-900 dark:text-white md:text-7xl mb-6">
          Don’t make connecting awkward</h1>
        <p class="mt-4 text-lg md:text-xl font-normal text-primary-500 md:max-w-3xl md:mx-auto mb-6 md:mb-10">No more
          fumbling for business cards or searching for lost contacts after an event. Robow makes it easy to exchange info
          and keep the conversation going straight from your inbox.</p>
        <a class="text-white bg-primary-900 hover:bg-jive-green focus:ring-4 focus:outline-none focus:ring-jive-teal/30 font-semibold rounded-full text-xl px-12 py-4 text-center dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 inline-block transition"
          style="    padding: 15px;
    margin-left: 30%;">Sign
          up free</a>
      </div>
    </header>
    <div class="mt-8 sm:mt-16">
      <div class="relative mx-auto max-w-[800px] w-auto">
        <img src="/img/robowReview.png" class="w-full" style="margin-left: 30%;">
      </div>
    </div>
    <div
      class="my-8 lg:my-12 gap-8 flex flex-col md:flex-row flex-wrap md:gap-12 justify-center content-center justify-items-center">
      <div class="max-w-[310px]">
        <img src="https://www.letsjive.io/images/marketing/feature-1.svg" class="mx-auto mb-4 w-12 h-12" alt="Step 1">
        <h3 class="mb-2 text-2xl font-bold">Scan the QR code</h3>
        <p class="mb-4 text-primary-500 text-lg">When it’s time to swap info, have your new contact scan your QR code
          with their phone camera.</p>
      </div>
      <div class="max-w-[310px]">
        <img src="https://www.letsjive.io/images/marketing/feature-2.svg" class="mx-auto mb-4 w-12 h-12" alt="Step 2">
        <h3 class="mb-2 text-2xl font-bold">Send a message</h3>
        <p class="mb-4 text-primary-500 text-lg">Your QR code is linked to a custom message you’ve created. So all they
          have to do is hit <i>Send</i>.</p>
      </div>
      <div class="max-w-[310px]">
        <img src="https://www.letsjive.io/images/marketing/feature-3.svg" class="mx-auto mb-4 w-12 h-12" alt="Step 3">
        <h3 class="mb-2 text-2xl font-bold">Follow-up from your inbox</h3>
        <p class="mb-4 text-primary-500 text-lg">At the end of the event, you can quickly scan your inbox and reply to
          everyone you met.</p>
      </div>
    </div>
    <a href="https://www.letsjive.io/app/signup"
      class="text-white bg-primary-900 hover:bg-jive-pink focus:ring-4 focus:outline-none focus:ring-jive-teal/30 font-semibold rounded-full text-xl px-12 py-4 text-center dark:bg-primary-600 dark:hover:bg-primary-700 dark:focus:ring-primary-800 transition inline-block"
      style="margin-left: 45%; margin-top: 5%;">Start Robow</a>
    <footer class="p-4 md:p-8 lg:p-10 relative">
      <div class="mx-auto max-w-screen-xl text-center">
        <div class="flex items-center justify-center">
          <p v-if="!isMobile()" style="color: brown; font-size:30px; font-family:Georgia, serif,bold;">ROBOW</p>
            <p v-else style="color: brown; font-size:10px; font-family:Georgia, serif,bold;">ROBOW</p>
        </div>
        <p class="my-4 md:my-6 text-gray-500 dark:text-gray-400">Get connected and start Robow.</p>
        <span class="text-sm text-gray-500 sm:text-center ">© 2024 <a href="https://www.letsjive.io/"
            class="transition">Robow</a> by <a href="https://www.plainsightventures.co/"
            class="transition" target="_blank">Plain Sight Ventures</a></span>
      </div>
    </footer>
  </div>
</template>
