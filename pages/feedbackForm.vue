<template>
  <Feedback
    :bookingid="id"
  />
</template>
<script>
export default {
  data () {
    return {
      id: ''
    }
  },
  mounted () {
    this.id = this.$route.params.bookingid
    console.log(this.id)
  }
}
</script>
