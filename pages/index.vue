<template>
  <div>
    <NavBar />
    <!-- <HomePage /> -->
    <Carousel />
    <HotelService />
    <About />
    <Footer />
  </div>
</template>

<script>
export default {
  mounted () {
    localStorage.setItem('token', 'null')
  }
}
</script>
