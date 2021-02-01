<template>
  <Navbar />
  <router-view />
  <Footer />
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
:root {
  --orange: #ff5b22;
  --blue: #0077ff;
  --black-1: #1b1c1e;
  --black-2: #1f1f1f;
  --black-3: #2b2b2b;
  --black-4: #303030;
}
* {
  padding: 0px;
  margin: 0px;
  text-decoration: unset;
  outline: none;
  box-sizing: border-box;
}
html {
  height: 100%;
  width: 100%;
}
body {
  height: 100%;
  width: 100%;
  background-color: #f7f7f7;
  overflow-x: hidden;
  font-family: "Open Sans", sans-serif;
}
a,
button {
  color: inherit;
  border: unset;
  cursor: pointer;
}
svg {
  fill: currentColor;
}
img {
  max-width: 100%;
}
ul {
  padding-left: 20px;
}
</style>