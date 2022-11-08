<template>
  <div>
    <NavBar />
    <AllContactUs :customerid="customerID" />
    <Footer />
  </div>
</template>

<script>
export default {
  data () {
    return {
      customerID: ''
    }
  },
  created () {
    this.customerID = this.$route.params.customerid
    console.log(this.customerID)
  }
}
</script>
