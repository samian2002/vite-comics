<template>
  <main class="main-content">
    <!-- Sezione Jumbotron -->
    <section class="jumbotron text-center mb-4">
      <img src="/img/jumbotron.jpg" alt="Jumbotron" class="jumbotron-img">
    </section>
    
    <!-- Sezione delle serie correnti -->
    <section class="current-series container">
      <h2 class="section-title text-center bg-primary text-white py-2 mb-4">Current Series</h2>
      <div class="row">
        <!-- Card dei fumetti -->
        <div class="col-6 col-md-4 col-lg-2 mb-4" v-for="comic in comics" :key="comic.series">
          <div class="card h-100">
            <img :src="comic.thumb" :alt="comic.series" class="card-img-top comic-image">
            <div class="card-body">
              <h5 class="card-title">{{ comic.series }}</h5>
            </div>
          </div>
        </div>
      </div>
      <div class="text-center">
        <button class="btn btn-primary btn-lg">Load More</button>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'MainContent',
  data() {
    return {
      comics: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ]
    }
  }
}
</script>

<style scoped>
.main-content {
  background-color: #36454f; 
  color: black;
  padding: 20px; 
}

.jumbotron {
  margin-bottom: 30px;
}

.jumbotron-img {
  width: 100%;
  height: 300px; 
  object-fit: cover; 
}

.section-title {
  font-size: 24px;
  padding: 10px;
}

.comic-image {
  height: 200px;
  object-fit: cover;
}
</style>
