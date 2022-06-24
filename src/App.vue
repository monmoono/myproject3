<template>
  <body>
    <nav>
      <div class="container">
        <div class="topnav">
          <a class="active" href="#">Home</a>
          <a href="#contact">Contact</a>
          <a href="#about">About</a>
        </div>
      </div>
    </nav>
    <main>
      <section id="wrap-main" class="wrap-main">
        <!-- start left bar -->
        <div class="left-bar">
          <div class="card-area-left">
            <h1 class="card-title-center">286x180</h1>
          </div>
          <div class="card-area">
            <h2 class="card-title">This is Exam Question 6 "Card"</h2>
            <div class="card-text">
              <p style="margin-bottom: 15px">
                And this is Exam Question 2 "Modal".
                <br />If you want to see the results of Question 2, press the
                button.
              </p>
              <button class="btn primary">Go to Modal</button>
            </div>
          </div>
        </div>
        <!-- end left bar -->

        <!-- start center -->
        <div class="center-bar">
          <div class="carousel-img">
            <carousel>
              <carousel-slide
                v-for="slide in slides"
                :key="slide"
                class="carousel-slider"
              >
                <h2 class="card-title">This is Exam Question 7 "Slider"</h2>
                <img :src="slide" :alt="slide" />
              </carousel-slide>
            </carousel>
          </div>

          <div class="card-area">
            <h2 class="card-title">This is Exam Question 1 "Button"</h2>
            <div class="card-button">
              <button type="button" class="btn primary">Primary</button>
              <button type="button" class="btn secondary">Secondary</button>
              <button type="button" class="btn success">Success</button>
              <button type="button" class="btn danger">Danger</button>
              <button type="button" class="btn warning">Warning</button>
              <button type="button" class="btn info">Info</button>
              <button type="button" class="btn light">Light</button>
              <button type="button" class="btn dark">Dark</button>
              <button type="button" class="link">Link</button>
            </div>
          </div>
          <div class="card-form">
            <h2 class="card-title">This is Exam Question 4 "Form"</h2>

            <div class="card-in-form">
              <div class="input-name">
                <h1>First name</h1>
                <input class="name" />
              </div>
              <div class="input-name">
                <h1>Last name</h1>
                <input class="name" />
              </div>
              <div class="input-name">
                <h1>Username</h1>
                <input class="username" />
              </div>
            </div>

            <div class="card-in-form">
              <div class="input-name">
                <h1>City</h1>
                <input class="name" />
              </div>
              <div class="input-name">
                <h1>state</h1>
                <input class="name" />
              </div>
              <div class="input-name">
                <h1>Zip</h1>
                <input class="number" />
              </div>
            </div>

            <div class="button-form">
              <button type="button" class="btn success">Submit form</button>
              <button type="button" class="btn danger" style="margin-left: 20px">Reset</button>
            </div>
          </div>

          <div class="card-footer">
            <div class="card-text-footer">
              <h2 class="card-title">This is Exam Question 3 "Pagination"</h2>
              <div class="card-text" style="margin-bottom: 15px">
                If you want to see the results of Problem 4, change the
                Pagination to the next page.
                <div class="pagination-center">
                  <div class="pagination">
                    <a href="#">&laquo;</a>
                    <a href="#" class="active">1</a>
                    <a href="#">2</a>
                    <a href="#">&raquo;</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- end center -->
      </section>
    </main>
  </body>
</template>

<script>
import Carousel from "./components/Carousel.vue";
import CarouselSlide from "./components/CarouselSlide.vue";
export default {
  data() {
    return {
      slides: [
        "https://picsum.photos/id/240/1168/500",
        "https://picsum.photos/id/241/1168/500",
        "https://picsum.photos/id/242/1168/500",
      ],
      visivleSlide: 0,
    };
  },
  components: {
    Carousel: Carousel,
    CarouselSlide: CarouselSlide,
  },
};
</script>

<style lang="sass">
@import './src/assets/main.sass'
</style>
