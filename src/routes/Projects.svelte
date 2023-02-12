<script>
  import { onMount } from "svelte";
  import TypeIt from "typeit";
  onMount(() => {
    new TypeIt("#projects", {
      strings: "projects",
      speed: 100,
      breakLines: false,
      waitUntilVisible: true,
      startDelete: false,
    }).go();
  });
</script>

<div class="py-8  text-5xl font-black ">
  <div class="flex gap-2 items-center">
    <div>></div>
    <div id="projects" class="py-7" />
  </div>
</div>
<div class="grid border grid-cols-7 ">
  <div class="h-full border">
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Gift Inventory System
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Lead Managment System
    </div>
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      E-Voting System
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Mind Castle
    </div>
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Speechinator - 4000
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Read Easy
    </div>
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
  </div>
  <div class=" h-full border">
    <div
      class="border h-1/4 flex items-center justify-center hover:bg-purple-500 cursor-pointer "
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
        />
      </svg>
    </div>
    <div
      class="text text-3xl border h-3/4 w-full flex items-center justify-center"
    >
      Womaniya
    </div>
  </div>
</div>
<div
  class="flex gap-3 items-center hover:text-purple-500 transition-all cursor-pointer py-10"
>
  <div class="text-xl">There's more on my GitHub</div>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="1.5"
    stroke="currentColor"
    class="w-6 h-6"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
    />
  </svg>
</div>

<style>
  .text {
    writing-mode: vertical-rl;
    text-orientation: mixed;
  }
</style>
