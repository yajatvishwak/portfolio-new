<script>
  import WebdevWorkshop from "./achievementdeets/WebdevWorkshop.svelte";
  import QuantumX from "./achievementdeets/QuantumX.svelte";
  import Visionet from "./achievementdeets/Visionet.svelte";
  import { onMount } from "svelte";
  import TypeIt from "typeit";

  onMount(() => {
    new TypeIt("#achievements", {
      strings: "achievements",
      speed: 100,
      breakLines: false,
      waitUntilVisible: true,
      startDelete: false,
    }).go();
  });
</script>

<div class="flex flex-col">
  <div class="py-16  text-5xl font-black ">
    <div class="flex gap-2 items-center">
      <div>></div>
      <div id="achievements" class="py-7" />
    </div>
  </div>
  <Visionet />
  <QuantumX />
  <WebdevWorkshop />
</div>
