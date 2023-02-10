<script>
  import a1 from "../../assets/achievments/1.jpeg";
  import a2 from "../../assets/achievments/2.jpeg";
  import a3 from "../../assets/achievments/3.jpeg";
  import a4 from "../../assets/achievments/4.jpeg";
  import a5 from "../../assets/achievments/5.jpeg";
  import a6 from "../../assets/achievments/6.jpeg";
  import a7 from "../../assets/achievments/7.jpeg";
  import a8 from "../../assets/achievments/8.jpeg";
</script>

<div id="wrapper">
  <div id="top-oval" />
  <div id="strip-w">
    <div id="strip-item">
      <img src={a1} />
    </div>
    <div id="strip-item">
      <img src={a2} />
    </div>
    <div id="strip-item">
      <img src={a3} />
    </div>
    <div id="strip-item">
      <img src={a4} />
    </div>
    <div id="strip-item">
      <img src={a5} />
    </div>
    <div id="strip-item">
      <img src={a6} />
    </div>
    <div id="strip-item">
      <img src={a7} />
    </div>
    <div id="strip-item">
      <img src={a8} />
    </div>
  </div>
  <div id="bottom-oval" />
</div>

<style>
  #wrapper {
    width: 100%;
    height: 320px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
  }

  #top-oval {
    position: absolute;
    top: 0;
    height: 50px;
    width: 100%;
    background: black;
    border-bottom-left-radius: 70%;
    border-bottom-right-radius: 70%;
  }
  #bottom-oval {
    position: absolute;
    bottom: 0;
    height: 50px;
    width: 100%;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
    background: black;
  }

  #strip-w {
    width: 100%;
    min-width: 1200px;
    height: 300px;
    display: flex;
    flex-wrap: no-wrap;
    align-items: flex-start;
    overflow-x: auto;
  }

  #strip-item {
    height: 300px;
    width: 300px;
    min-width: 300px;
    margin-right: 10px;
    background: green;
    overflow: hidden;
    /* background-size: cover; */
    /* background-image: url(https://images.unsplash.com/photo-1470848051974-964b789cb6fa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2071&q=80); */
  }
  #strip-item > img {
    height: 100%;
    width: 100%;
    object-fit: cover;
  }
</style>
