<template>
  <main class="layout" role="main">
    <div class="backgraund-drilling-line"></div>
    <div class="backgraund-drilling-point"></div>
    <slot/>
    <div class="footer">
      <p>
        Made by umzo
        <!-- <a class="link" href="//twitter.com/lauragift_">github</a> -->
      </p>
    </div>
  </main>
</template>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
}
.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
.footer {
  padding-top: calc(30em / 4);
  text-align: center;
  font-size: 1em;
}
.backgraund-drilling-line{
  top: 20px;
  left: -30px;
  width: 451px;
  height: 100px;
  display: inline-block;
  background: #5AB574;
  transform: rotateZ(45deg);
  position: fixed;
  z-index: -999;
}
.backgraund-drilling-point{
  top: 221.5px;
  left: 321.8px;
  width: 0;
  height: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-bottom: 50px solid #5AB574;
  display: inline-block;
  transform: rotateZ(135deg);
  position: fixed;
  z-index: -999;
}
</style>