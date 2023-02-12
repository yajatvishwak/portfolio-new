<script>
  import { onMount } from "svelte";
  import TypeIt from "typeit";

  onMount(() => {
    new TypeIt("#skills", {
      strings: "skills",
      speed: 75,
      breakLines: false,
      startDelete: false,
      waitUntilVisible: true,
    }).go();
  });
</script>

<div class=" h-full">
  <div class="">
    <div class="flex gap-2 items-center py-16 text-5xl font-bold ">
      <div>></div>
      <div id="skills" />
    </div>
  </div>

  <div class="grid grid-cols-3 w-full h-[80vh]">
    <div
      class="border bg-[#E6FF82] text-black font-black flex items-center justify-center text-4xl"
    >
      Databases
    </div>
    <div class="border" />
    <div class="border" />
    <div class="border" />
    <div
      class="border bg-[#7E41FF] text-black font-black flex items-center justify-center text-4xl"
    >
      Frameworks
    </div>
    <div class="border" />
    <div class="border" />
    <div class="border" />
    <div
      class="border bg-[#5DF0B2] text-black font-black flex items-center justify-center text-4xl"
    >
      Tools
    </div>
  </div>
</div>
