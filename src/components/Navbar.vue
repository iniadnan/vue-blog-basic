<template>
  <nav id="navbar">
    <div class="navbar__left">
      <h1><router-link to="/">RoadRoad</router-link></h1>
    </div>
    <div class="navbar__right">
      <div class="navbar__list">
        <router-link to="/" class="navbar__link">Home</router-link>
        <router-link to="/" class="navbar__link">About</router-link>
        <router-link to="/" class="navbar__link">Gallery</router-link>
        <router-link to="/" class="navbar__link">Contact</router-link>
      </div>
      <button class="navbar__button">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="currentColor"
          class="bi bi-search"
          viewBox="0 0 16 16"
        >
          <path
            d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
          />
        </svg>
      </button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
#navbar {
  height: 80px;
  width: 100vw;
  display: flex;
  background-color: #fff;
}
.navbar__left {
  flex-basis: 40%;
  display: flex;
  align-items: center;
  padding-left: 48px;
}
.navbar__left h1 {
  font-weight: 600;
  font-size: 2em;
  letter-spacing: 1.5px;
  color: var(--black-1);
}
.navbar__right {
  height: 100%;
  flex-basis: 60%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.navbar__link {
  margin-right: 32px;
  font-weight: 500;
  font-size: 1.1em;
  letter-spacing: 1px;
  color: var(--black-2);
}
.navbar__button {
  position: relative;
  padding: 0px 48px;
  height: 100%;
  background-color: var(--orange);
  color: #fff;
}
.navbar__button svg {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>