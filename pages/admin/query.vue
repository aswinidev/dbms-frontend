<template>
  <div>
    <div v-if="getDetails===false">
      <div class="page">
        <h1>Customer Queries</h1>
      </div>
      <BookingList
        v-for="booking in bookings"
        :key="booking.bookingID"
        :bookingid="booking.bookingID"
        :checkin="booking.checkInDate"
        :checkout="booking.checkOutDate"
        @clicked="onClickListItem(booking.bookingID)"
      />
    </div>
    <div v-else>
      <button class="custom-btn btn-1" @click="goBacktoPage">
        <span>Back</span>
      </button>
      <BookingDetails :bookingid="id" />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      getDetails: false,
      bookings: [],
      id: ''
    }
  },
  mounted () {
    // getmapping
  },
  methods: {
    onClickListItem (value) {
      this.getDetails = true
      this.id = value
    },
    goBacktoPage () {
      this.getDetails = false
    }
  }

}
</script>

<style scoped>
    @import '@/assets/booking/bookingList.css'
</style>
