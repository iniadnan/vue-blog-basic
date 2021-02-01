<template>
  <footer id="footer">
    <div class="footer__left">
      <h4><router-link to="/">RoadRoad</router-link></h4>
    </div>
    <div class="footer__right">
      <div class="footer__list">
        <router-link to="/" class="footer__link">Home</router-link>
        <router-link to="/" class="footer__link">About</router-link>
        <router-link to="/" class="footer__link">Gallery</router-link>
        <router-link to="/" class="footer__link">Contact</router-link>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
#footer {
  height: 70px;
  width: 100%;
  display: flex;
  background-color: #fff;
  padding: 0px 48px;
}
.footer__left {
  flex-basis: 50%;
  display: flex;
  align-items: center;
}
.footer__left h4 {
  font-weight: 600;
  font-size: 1.5em;
  letter-spacing: 1.25px;
  color: var(--orange);
}
.footer__right {
  height: 100%;
  flex-basis: 60%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.footer__link {
  margin-right: 32px;
  font-weight: 500;
  font-size: 1.1em;
  letter-spacing: 1px;
  color: var(--black-2);
}
</style>