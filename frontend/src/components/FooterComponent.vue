<template>
  <div class="footer">
    <div class="news-letter"></div>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "FooterComponent",

  computed: {
    ...mapState(["user"]),
  },

  methods: {
    scrollToTop() {
      window.scrollTo(0, 0);
    },
  },
};
</script>

<style scoped>
/* footer */
.footer {
  background: #f7f7f7;
  padding: 2rem 9%;
}

.footer .news-letter {
  text-align: center;
  margin-bottom: 2rem;
}

.footer .news-letter h3 {
  font-size: 2.5rem;
  color: #130f40;
  padding-bottom: 1rem;
}

.footer .news-letter form {
  max-width: 70rem;
  margin: 1rem auto;
  max-width: 70rem;

  display: flex;
  border-radius: 0.5rem;
  overflow: hidden;
}

.footer .news-letter form input[type="email"] {
  height: 100%;
  width: 100%;
  padding: 1rem 1.2rem;
  font-size: 1.6rem;
  color: #130f40;
  text-transform: none;
}

.footer .news-letter form input[type="submit"] {
  padding: 0 2rem;
  font-size: 1.6rem;
  color: #fff;
  background: #27ae60;
  cursor: pointer;
}

.footer .news-letter form input[type="submit"]:hover {
  background: #130f40;
}

.footer .box-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
  gap: 1.5rem;
}

.footer .box-container .box h3 {
  font-size: 2.2rem;
  color: #130f40;
  padding: 1rem 0;
}

.footer .box-container .box p {
  font-size: 1.4rem;
  color: #666;
  padding: 1rem 0;
}

.footer .box-container .box a {
  display: block;
  font-size: 1.4rem;
  color: #666;
  padding: 1rem 0;
}

.footer .box-container .box a:hover {
  color: #27ae60;
}

.footer .box-container .box a:hover i {
  padding-right: 2rem;
}

.footer .box-container .box a i {
  padding-right: 0.5rem;
  color: #27ae60;
}

.footer .bottom {
  padding-top: 1rem;
  text-align: center;
}

.footer .bottom .share {
  margin: 1.5rem 0;
}

.footer .bottom .share a {
  height: 4.5rem;
  width: 4.5rem;
  line-height: 4.5rem;
  font-size: 2rem;
  border-radius: 0.5rem;
  margin: 0 0.3rem;
  color: #fff;
  background: #27ae60;
}

.footer .bottom .share a:hover {
  background: #130f40;
}

@media (max-width: 576px) {
  .footer .box-container {
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
  }
}
</style>
