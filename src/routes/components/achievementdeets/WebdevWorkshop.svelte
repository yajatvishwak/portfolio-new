<script>
  import a3 from "../../../assets/achievments/3.jpeg";
  let image;
  function handleMove(e, cursor) {
    let x = e.pageX;
    var y = e.pageY;
    cursor.style.top = `${y - 50}px`;
    cursor.style.left = `${x - 50}px`;
  }
</script>

<div class="border-y-2  py-10 px-4 flex  items-center justify-between">
  <div
    on:mousemove={(e) => handleMove(e, image)}
    class="group w-full  flex justify-between  overflow-hidden"
  >
    <div class="text-3xl  group-hover:text-purple-600 transition-all z-10">
      Web Dev Workshop, 2023
    </div>

    <img
      bind:this={image}
      src={a3}
      alt=""
      class="opacity-0 rounded-2xl group-hover:opacity-100 z-0 -translate-x-1/2 -translate-y-1/2  box-border transition-all absolute w-1/3 object-cover"
    />
  </div>
  <div class=" w-full text-right group-hover:text-purple-600">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      stroke-width="1.5"
      stroke="currentColor"
      class="w-6 h-6 ml-auto"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M4.5 19.5l15-15m0 0H8.25m11.25 0v11.25"
      />
    </svg>
  </div>
</div>
