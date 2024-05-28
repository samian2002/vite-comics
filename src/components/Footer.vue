<template>
  <footer class="footer text-white">
    <div class="footer-top py-4">
      <div class="container">
        <div class="row">
          <!-- Sezioni di link, 2 per riga sui dispositivi mobili -->
          <div class="col-6 col-md-3" v-for="section in linkSections" :key="section.title">
            <h5 class="section-title">{{ section.title }}</h5>
            <ul class="list-unstyled">
              <li v-for="link in section.links" :key="link">{{ link }}</li>
            </ul>
          </div>

          <div class="col-6 col-md-3 d-md-flex align-items-center justify-content-center d-none d-md-block">
            <img src="/img/dc-logo-bg.png" alt="DC Logo Background" class="footer-logo">
          </div>

          <div class="col-12 d-block d-md-none text-center mt-4">
            <img src="/img/dc-logo-bg.png" alt="DC Logo Background" class="footer-logo">
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom py-3 bg-dark">
      <div class="container d-flex justify-content-between align-items-center flex-wrap">
        <div class="social-section mb-3 mb-md-0">
          <h5 class="section-title mb-3">Follow Us</h5>
          <div class="d-flex">
            <a href="#" class="me-3">
              <img src="/img/footer-facebook.png" alt="Facebook" class="social-icon">
            </a>
            <a href="#" class="me-3">
              <img src="/img/footer-twitter.png" alt="Twitter" class="social-icon">
            </a>
            <a href="#" class="me-3">
              <img src="/img/footer-youtube.png" alt="YouTube" class="social-icon">
            </a>
            <a href="#" class="me-3">
              <img src="/img/footer-pinterest.png" alt="Pinterest" class="social-icon">
            </a>
            <a href="#">
              <img src="/img/footer-periscope.png" alt="Periscope" class="social-icon">
            </a>
          </div>
        </div>
        <button class="btn btn-primary btn-lg">Sign-Up Now!</button>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      linkSections: [
        {
          title: "DC COMICS",
          links: [
            "Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"
          ]
        },
        {
          title: "DC",
          links: [
            "Terms Of Use", "Privacy Policy", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops"
          ]
        },
        {
          title: "SITES",
          links: [
            "DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"
          ]
        }
      ]
    }
  }
}
</script>

<style scoped>
.footer {
  background: url('/img/footer-bg.jpg') no-repeat center center;
  background-size: cover;
}

.footer-top {
  border-bottom: 1px solid #444;
}

.footer-logo {
  width: 100px;
}

.footer-bottom {
  background-color: #333;
}

.social-section {
  text-align: left;
}

.social-icon {
  width: 30px;
  height: 30px;
}

.btn-primary {
  background-color: #0282f9;
  border: none;
  text-transform: uppercase;
}

.btn-primary:hover {
  background-color: #026bb5;
}

.section-title {
  font-size: 1.25rem;
  font-weight: bold; 
}
</style>
