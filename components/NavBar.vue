<template>
  <div id="app">
    <section class="navigation">
      <div class="nav-container">
        <div class="brand">
          <a href="#">
            <h1>Le Lotus Grand</h1>
          </a>
        </div>

        <nav>
          <div class="nav-mobile">
            <a id="nav-toggle" href="#"><span /></a>
          </div>

          <div class="menu-main-menu-container">
            <ul class="nav-list">
              <li><a href="#">Home</a></li>
              <li><a href="#">About</a></li>
              <li><a href="#">Booking</a></li>
              <li><a href="#">Contact Us</a></li>
              <li>
                <a href="#">Login/Register</a>
              </li>
            </ul>
          </div>
        </nav>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      activeDropdown: null
    }
  },
  methods: {
    toggleActiveDropdown (dropdown) {
      this.activeDropdown = this.activeDropdown === dropdown ? null : dropdown
    }
  }
}
</script>

<style>
    @import '@/assets/NavBar/navbar.css';
</style>
