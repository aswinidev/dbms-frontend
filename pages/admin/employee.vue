<template>
  <div>
    <NavBar />
    <div v-if="getDetails==false">
      <!-- <div class="page">
        <div class="buttons">
          <a class="btn add-new" href="/booking-form">Add New Booking</a>
        </div>
      </div> -->
      <EmployeeList />
      <EmployeeList
        v-for="employee in employees"
        :key="employee.employeeID"
        :employeeid="employee.employeeID"
        :checkin="booking.checkInDate"
        :checkout="booking.checkOutDate"
        @clicked="onClickListItem(booking.bookingID)"
      />
    </div>
    <div v-else>
      <button class="custom-btn btn-1" @click="goBacktoPage">
        <span>Back</span>
      </button>
      <EmployeeDetails :bookingid="id" />
    </div>

    <Footer />
  </div>
</template>

<script>
import EmployeeList from '~/components/EmployeeList.vue'

export default {
  components: { EmployeeList },
  data () {
    return {
      getDetails: false,
      employees: [],
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
