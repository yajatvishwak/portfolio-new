<script>
  import a1 from "../../assets/achievments/1.jpeg";
  import a2 from "../../assets/achievments/2.jpeg";
  import a3 from "../../assets/achievments/3.jpeg";
  import a4 from "../../assets/achievments/4.jpeg";
  import a5 from "../../assets/achievments/5.jpeg";
  import a6 from "../../assets/achievments/6.jpeg";
  import a7 from "../../assets/achievments/7.jpeg";
  import a8 from "../../assets/achievments/8.jpeg";
  let currentSlide = 0;
  // let slides = [
  //   { id: 0, src: a1, alt: "Image 1", text: "Image 1", class: "img1" },
  //   { id: 1, src: a2, alt: "Image 2", text: "Image 2", class: "img2" },
  //   { id: 2, src: a3, alt: "Image 3", text: "Image 3", class: "img3" },
  //   { id: 3, src: a4, alt: "Image 3", text: "Image 3", class: "img3" },
  //   { id: 4, src: a5, alt: "Image 3", text: "Image 3", class: "img3" },
  //   { id: 5, src: a6, alt: "Image 3", text: "Image 3", class: "img3" },
  //   { id: 6, src: a7, alt: "Image 3", text: "Image 3", class: "img3" },
  //   { id: 7, src: a8, alt: "Image 3", text: "Image 3", class: "img3" },
  //   // Add more slides as needed
  // ];

  // function handlePrev() {
  //   currentSlide = currentSlide === 0 ? slides.length - 1 : currentSlide - 1;
  // }

  // function handleNext() {
  //   currentSlide = currentSlide === slides.length - 1 ? 0 : currentSlide + 1;
  // }
  let mouseDownAt = 0;
  let previousPercentage = 0;
  let percentage = 0;
  let track;

  $: {
    console.log({ mouseDownAt, previousPercentage, percentage });
  }
  const handleOnDown = (e) => {
    mouseDownAt = e.clientX;
  };
  const handleOnUp = () => {
    mouseDownAt = 0;
    previousPercentage = percentage;
  };
  const handleOnMove = (e) => {
    if (mouseDownAt === 0) return;

    const mouseDelta = parseFloat(mouseDownAt) - e.clientX,
      maxDelta = document.body.clientWidth / 2;

    const percent = (mouseDelta / maxDelta) * -100,
      nextPercentageUnconstrained = parseFloat(previousPercentage) + percent,
      nextPercentage = Math.max(Math.min(nextPercentageUnconstrained, 0), -100);

    percentage = nextPercentage;

    track.animate(
      {
        transform: `translate(${nextPercentage}%, -50%)`,
      },
      { duration: 1200, fill: "forwards" }
    );
    for (const image of track.getElementsByClassName("image")) {
      image.animate(
        {
          objectPosition: `${100 + nextPercentage}% center`,
        },
        { duration: 1200, fill: "forwards" }
      );
    }
  };
</script>

<div
  on:mousedown={handleOnDown}
  on:mouseup={handleOnUp}
  on:mousemove={handleOnMove}
  on:touchstart={(e) => handleOnDown(e.touches[0])}
  on:touchend={(e) => handleOnUp(e.touches[0])}
  on:touchmove={(e) => handleOnMove(e.touches[0])}
  bind:this={track}
  id="image-track"
>
  <img src={a1} class="object-cover image" draggable="false" alt="" />
  <img src={a2} class="object-cover image" draggable="false" alt="" />
  <img src={a3} class="object-cover image" draggable="false" alt="" />
  <img src={a4} class="object-cover image" draggable="false" alt="" />
  <img src={a6} class="object-cover image" draggable="false" alt="" />
  <img src={a7} class="object-cover image" draggable="false" alt="" />
  <img src={a8} class="object-cover image" draggable="false" alt="" />
</div>

<style>
  #image-track {
    display: flex;
    background-color: aqua;
    width: 100vh;
    gap: 4vmin;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(0%, -50%);
    user-select: none; /* -- Prevent image highlighting -- */
  }
  #image-track > .image {
    width: 30vmin;
    height: 56vmin;
    object-fit: cover;
    object-position: 100% center;
  }
</style>
