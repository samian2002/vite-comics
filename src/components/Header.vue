<template>
  <header class="bg-white border-bottom">
    <!-- Container principale del header -->
    <div class="container d-flex justify-content-between align-items-center py-3">
      <!-- Logo DC Comics -->
      <img src="/img/dc-logo.png" alt="DC Comics Logo" class="logo">
      
      <!-- Navigazione per schermi medi e grandi -->
      <nav class="d-none d-md-block">
        <ul class="nav">
          <li class="nav-item" v-for="link in links" :key="link.text">
            <a :href="link.url" class="nav-link text-dark">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
      
      <!-- Bottone menu hamburger per schermi piccoli-->
      <button class="navbar-toggler d-md-none" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <i class="fas fa-bars"></i>
      </button>
    </div>
    
    <!-- Menu collapsible per schermi piccoli -->
    <div class="collapse d-md-none" id="navbarNav">
      <ul class="nav flex-column">
        <li class="nav-item" v-for="link in links" :key="link.text">
          <a :href="link.url" class="nav-link text-dark">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      links: [
        { text: 'Characters', url: '#' },
        { text: 'Comics', url: '#' },
        { text: 'Movies', url: '#' },
        { text: 'TV', url: '#' },
        { text: 'Games', url: '#' },
        { text: 'Collectibles', url: '#' },
        { text: 'Videos', url: '#' },
        { text: 'Fans', url: '#' },
        { text: 'News', url: '#' },
        { text: 'Shop', url: '#' }
      ]
    }
  }
}
</script>

<style scoped>
.logo {
  height: 50px;
}

.navbar-toggler {
  border: none;
  background: none; 
}

.navbar-toggler:focus {
  outline: none;
}

.fas.fa-bars {
  color: #36454f; 
  font-size: 24px; 
}
</style>
