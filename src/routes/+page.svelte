<script>
  import { onMount } from "svelte";

  import logo from "../assets/logo.svg";
  import star from "../assets/star.svg";
  import me from "../assets/me.png";
  import menu from "../assets/menu.svg";
  import Achievements from "./components/Achievements.svelte";

  // variable declaration
  let profileimage;

  let cursorPosition = { x: 0, y: 0 };
  let width;
  let height;

  // helpers and handlers
  function handleMousemove(event) {
    cursorPosition.x = event.clientX;
    cursorPosition.y = event.clientY;
  }

  // you know what this is.
  onMount(() => {
    width =
      window.innerWidth ||
      document.documentElement.clientWidth ||
      document.body.clientWidth;
    height =
      window.innerHeight ||
      document.documentElement.clientHeight ||
      document.body.clientHeight;
  });
  // reactive changes
  $: {
    //console.log(cursorPosition);
    if (profileimage && width && height) {
      profileimage.style.setProperty(
        "--xoffset",
        `${(cursorPosition.x / width) * 40 - 20}px`
      );
      profileimage.style.setProperty(
        "--yoffset",
        `${(cursorPosition.y / height) * 40 - 20}px`
      );
    }
  }
</script>

<main
  on:mousemove={handleMousemove}
  class="bg-black text-white h-full min-h-screen overflow-hidden"
>
  <nav class="flex w-full fixed justify-between px-32 py-10">
    <div>
      <img src={logo} class="w-10" alt="" />
    </div>
    <div class="flex flex-col items-end text-3xl">
      <div>Portfolio of Yajat</div>
      <div>Vishwakarma</div>
    </div>
  </nav>
  <!-- Introduction page -->
  <section class="flex flex-col justify-center items-center h-screen">
    <img
      src={me}
      bind:this={profileimage}
      class="w-1/6  -mt-20 mb-5 meshadow "
      alt=""
    />
    <div class="text-9xl">Hello World.</div>
    <div class="flex gap-5 mt-3">
      <div class="text-3xl">web dev</div>
      <div class=""><img src={star} alt="" /></div>
      <div class="text-3xl">BLR, india</div>
    </div>
  </section>

  <section class="h-screen  ">
    <div class="flex flex-col justify-center items-center">
      <div class="py-14 px-4 text-5xl">whoami</div>
      <div class="flex flex-col gap-10 max-w-screen-lg">
        <div class="flex gap-4 items-center">
          <img src={star} class="w-20" alt="" srcset="" />
          <div class="text-3xl ">
            <span class="opacity-60"> With a </span>
            <span class="opacity-100  font-semibold">love for technology,</span>

            <span class="opacity-60"
              >I am constantly learning and discovering new advancements to fuel
              my passion
            </span>
          </div>
        </div>
        <div class="flex gap-4 items-center">
          <img src={star} class="w-16" alt="" srcset="" />
          <div class="text-3xl">
            <span class="opacity-60">Mastered the art of</span>
            <span class="opacity-100 font-black ">web development </span>
            <span class="opacity-60">and have a particular affinity for </span>
            <span class="text-orange-500 opacity-100">Svelte JS</span>
          </div>
        </div>
        <div class="flex gap-4 items-center">
          <img src={star} class="w-20" alt="" srcset="" />
          <div class="text-3xl">
            <span class="opacity-100 font-bold">Fascinated by AI/ML,</span>
            <span class="opacity-60"
              >constantly seeking new ways to apply these technologies to solve
              intricate problems</span
            >
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="h-screen">
    <div class="py-16 px-4 text-5xl">Achievements</div>
    <Achievements />
  </section>

  <nav class="fixed bottom-0 right-0 px-32 py-10">
    <img src={menu} class="w-10" alt="" />
  </nav>
</main>

<style>
  .meshadow {
    border-radius: 100%;
    box-shadow: var(--xoffset) var(--yoffset) 250px 50px #7e41ff;
  }
</style>
