<template>
  <header id="header">
    <div class="header__cover">
      <div class="header__location">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          class="bi bi-geo-alt-fill"
          viewBox="0 0 16 16"
        >
          <path
            d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10zm0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6z"
          />
        </svg>
        <span>Where Are You</span>
      </div>
      <h2>
        I don't sleep at night Couse<br />
        I'm thinking of you.
      </h2>
      <div class="header__socialmedia">
        <router-link to="/">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill="currentColor"
            class="bi bi-facebook"
            viewBox="0 0 16 16"
          >
            <path
              d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"
            />
          </svg>
        </router-link>
        <router-link to="/">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill="currentColor"
            class="bi bi-instagram"
            viewBox="0 0 16 16"
          >
            <path
              d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"
            />
          </svg>
        </router-link>
      </div>
    </div>
  </header>
  <main id="main">
    <article
      class="main__article__list"
      v-for="photo in photos"
      :key="photo.id"
    >
      <div>
        <div class="main__article__image">
          <img :src="photo.url" :alt="photo.title" />
        </div>
        <div class="main__article__description">
          <h2>
            <router-link :to="{ name: 'Article', params: { id: photo.id } }">{{
              photo.title
            }}</router-link>
          </h2>
          <div class="main__article__description__information">
            <div>
              <img src="@/assets/iniadnan.jpg" alt="Adnan Muttaqin" />
              <span>Adnan Muttaqin</span>
            </div>
            <div>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="18"
                height="18"
                fill="currentColor"
                class="bi bi-hand-thumbs-up-fill"
                viewBox="0 0 16 16"
              >
                <path
                  d="M6.956 1.745C7.021.81 7.908.087 8.864.325l.261.066c.463.116.874.456 1.012.964.22.817.533 2.512.062 4.51a9.84 9.84 0 0 1 .443-.05c.713-.065 1.669-.072 2.516.21.518.173.994.68 1.2 1.273.184.532.16 1.162-.234 1.733.058.119.103.242.138.363.077.27.113.567.113.856 0 .289-.036.586-.113.856-.039.135-.09.273-.16.404.169.387.107.819-.003 1.148a3.162 3.162 0 0 1-.488.9c.054.153.076.313.076.465 0 .306-.089.626-.253.912C13.1 15.522 12.437 16 11.5 16H8c-.605 0-1.07-.081-1.466-.218a4.826 4.826 0 0 1-.97-.484l-.048-.03c-.504-.307-.999-.609-2.068-.722C2.682 14.464 2 13.846 2 13V9c0-.85.685-1.432 1.357-1.616.849-.231 1.574-.786 2.132-1.41.56-.626.914-1.279 1.039-1.638.199-.575.356-1.54.428-2.59z"
                />
              </svg>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="18"
                height="18"
                fill="currentColor"
                class="bi bi-suit-heart-fill"
                viewBox="0 0 16 16"
                style="margin-left: 18px"
              >
                <path
                  d="M4 1c2.21 0 4 1.755 4 3.92C8 2.755 9.79 1 12 1s4 1.755 4 3.92c0 3.263-3.234 4.414-7.608 9.608a.513.513 0 0 1-.784 0C3.234 9.334 0 8.183 0 4.92 0 2.755 1.79 1 4 1z"
                />
              </svg>
            </div>
          </div>
        </div>
      </div>
    </article>
  </main>
</template>

<script>
import axios from "axios";

export default {
  name: "Home",
  data() {
    return {
      photos: [],
    };
  },
  methods: {
    // dibuat seperti aja biar best practice dan berjalan secara asynchronus
    async getPhotos() {
      axios
        .get("https://jsonplaceholder.typicode.com/photos")
        .then((response) => {
          // langsung masukkin variable aja
          this.photos = response.data.slice(0, 9);
        })
        .catch((error) => console.log(error));
    },
  },
  created() {
    // taruh di lifecycle created aja biar lebih cepat loadnya
    this.getPhotos();
  },
};
</script>

<style scoped>
#header {
  height: 100vh;
  width: 100%;
  background-image: url("../assets/header.jpg");
  background-size: cover;
  background-position: center;
}
.header__cover {
  height: 100%;
  width: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0px 80px;
  background-color: rgba(0, 0, 0, 0.25);
}
.header__location {
  display: inline-flex;
  align-items: center;
  margin-bottom: 12px;
  font-weight: 600;
  font-size: 0.9em;
  text-transform: uppercase;
  color: var(--orange);
}
.header__location svg {
  margin-right: 12px;
}
.header__location span {
  color: #fff;
}
.header__cover h2 {
  margin-bottom: 24px;
  font-weight: 700;
  font-size: 2.5em;
  color: #fff;
}
.header__socialmedia a {
  margin-right: 12px;
  color: #fff;
}
#main {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  padding: 80px;
}
.main__article__list {
  flex-basis: 33.33%;
  padding: 12px;
  margin-bottom: 32px;
}
.main__article__list > div {
  width: 100%;
  display: flex;
  flex-direction: column;
  background-color: #fff;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
  overflow: hidden;
}
.main__article__list:nth-child(2) .main__article__image {
  order: 2;
}
.main__article__list:nth-child(5) .main__article__image {
  order: 2;
}
.main__article__list:nth-child(8) .main__article__image {
  order: 2;
}
.main__article__image img {
  height: 300px;
  width: 100%;
  display: block;
  object-fit: cover;
}
.main__article__description {
  padding: 24px 32px;
}
.main__article__description h2 {
  margin-bottom: 18px;
  font-size: 1.2em;
  font-weight: 600;
  line-height: 1.8;
  color: var(--black-2);
}
.main__article__description p {
  margin-bottom: 24px;
  font-size: 1em;
  font-weight: 400;
  line-height: 1.75;
  color: var(--black-3);
}
.main__article__description__information {
  display: flex;
  justify-content: space-between;
}
.main__article__description__information div {
  display: inline-flex;
  align-items: center;
  color: var(--black-4);
}
.main__article__description__information div img {
  height: 24px;
  width: 24px;
  object-fit: cover;
  border-radius: 50%;
}
.main__article__description__information div span {
  margin-left: 18px;
  font-size: 0.9em;
}
</style>