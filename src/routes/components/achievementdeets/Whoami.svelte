<script>
  import { onMount } from "svelte";
  import TypeIt from "typeit";

  onMount(() => {
    new TypeIt("#whoami", {
      strings: "whoami",
      speed: 75,
      breakLines: false,
      waitUntilVisible: true,
      startDelete: false,
    }).go();
  });
</script>

<div class="flex flex-col text-5xl ">
  <div class="flex gap-2 items-center py-16 font-extrabold">
    <div>></div>
    <div id="whoami" />
  </div>
  <div>
    <span class="opacity-50"
      >As a final year engineering student, I have a strong passion for</span
    >
    <span class="underline decoration-purple-500"
      >cooking, coding, innovating, and running.</span
    >
    <span class="opacity-50">
      I love exploring new ideas and finding ways to bring my passions to life.
    </span>
  </div>
  <div class="mt-10">
    <span class="opacity-50">Whether it's</span>
    <span class="underline decoration-purple-500">
      experimenting with new recipes in the kitchen, building the latest
      technology, or pushing my limits on the running trail,
    </span>
    <span class="opacity-50">
      I am constantly driven to learn and grow. I am eager to share my
      experiences and insights with others who share my interests.
    </span>
  </div>
</div>
