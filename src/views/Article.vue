<template>
  <main id="main">
    <article>
      <!-- HEADER ARTICLE -->
      <section class="main__header">
        <h1>{{ article.title }}</h1>
        <h3><router-link to="/">Write A Something</router-link></h3>
        <img :src="article.url" :alt="article.title" />
      </section>
      <!-- BODY ARTICLE -->
      <section class="main__body">
        <h2>
          It is a long established fact that a reader will be distracted by the
          readable content of a page when looking at its layout.
        </h2>
        <p>
          The point of using Lorem Ipsum is that it has a more-or-less normal
          distribution of letters, as opposed to using 'Content here, content
          here', making it look like readable English. It is a long established
          fact that a reader will be distracted by the readable content of a
          page when looking at its layout.
        </p>
        <p>
          Many desktop <a href="/">publishing packages</a> and web page editors
          now use Lorem Ipsum as their default model text, and a search for
          'lorem ipsum' will uncover many web sites still in their infancy.
          Various versions have evolved over the years, sometimes by accident,
          sometimes on purpose (injected humour and the like).
        </p>
        <p>
          Contrary to popular belief, Lorem Ipsum is not simply random text. It
          has roots in a piece of classical Latin literature from 45 BC, making
          it over 2000 years old.
        </p>
        <br />
        <img src="assets/images/kaiyu-wu-fJCOjH9Dwl0-unsplash.jpg" alt="#" />
        <br /><br />
        <h3>
          The standard chunk of Lorem Ipsum used since the 1500s is reproduced
          below for those interested.
        </h3>
        <p>
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book.
        </p>
        <p>
          It has survived not only five centuries, but also the leap into
          electronic typesetting, remaining essentially unchanged.
        </p>
        <p>
          It was popularised in the 1960s with the release of Letraset sheets
          containing Lorem Ipsum passages, and more recently with desktop
          publishing software like Aldus PageMaker including versions of Lorem
          Ipsum.
        </p>
        <br />
        <h3>
          Lorem Ipsum passage, and going through the cites of the word in
          classical literature
        </h3>
        <ul>
          <li>
            Contrary to popular belief, Lorem Ipsum is not simply random text.
          </li>
          <li>The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet.</li>
          <li>
            The standard chunk of Lorem Ipsum used since the 1500s is reproduced
            below for those interested.
          </li>
          <li>
            Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum
          </li>
        </ul>
      </section>
      <!-- FOOTER ARTICLE -->
      <section class="main__footer">
        <img src="@/assets/iniadnan.jpg" alt="Adnan Muttaqin" />
        <h6>"Terus Ingat, Bahwa Kita Bukan Siapa - Siapa"</h6>
        <h5>Adnan Muttaqin</h5>
      </section>
    </article>
  </main>
</template>

<script>
import axios from "axios";

export default {
  name: "Article",
  data() {
    return {
      article: [],
    };
  },
  methods: {
    // dibuat seperti aja biar best practice dan berjalan secara asynchronus
    async getArticles() {
      axios
        .get(
          "https://jsonplaceholder.typicode.com/photos/" + this.$route.params.id
        )
        // langsung masukan varible aja
        .then((response) => (this.article = response.data))
        .catch((error) => console.log(error));
    },
  },
  created() {
    // taruh di lifecycle created aja biar lebih cepat loadnya
    this.getArticles();
  },
};
</script>

<style scoped>
#main {
  width: 75%;
  display: flex;
  flex-wrap: wrap;
  padding: 80px;
  margin: 0px auto;
}
.main__header {
  width: 100%;
  text-align: center;
}
.main__header h1 {
  font-size: 2.4em;
  color: var(--black-1);
}
.main__header h3 {
  margin: 12px 0px 36px !important;
  font-size: 0.9em;
  color: var(--blue);
}
.main__header img {
  display: block;
  object-fit: cover;
  width: 100%;
}
.main__body {
  width: 100%;
  position: relative;
  padding: 32px !important;
}
.main__body h1,
.main__body h2,
.main__body h3,
.main__body h4,
.main__body h5,
.main__body h6 {
  margin-bottom: 24px !important;
}
.main__body p {
  line-height: 1.75;
  margin-block: 16px !important;
}
.main__footer {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 32px;
}
.main__footer img {
  height: 50px;
  width: 50px;
  display: block;
  border-radius: 50%;
}
.main__footer h5 {
  font-size: 1em;
  color: var(--blue);
}
.main__footer h6 {
  margin: 12px 0px 0px !important;
  font-size: 1em;
  color: var(--black-4);
}
</style>