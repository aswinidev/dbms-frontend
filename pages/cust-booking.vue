<template>
  <div class="container mt-4">
    <div class="text-center darken-grey-text mb-4">
      <h1 class="font-bold mt-4 mb-3 h1">
        <b>My Bookings ! </b>
      </h1>
      <br>
    </div>

    <div class="card mb-3">
      <div class="card-body">
        <!--Table-->
        <table class="table table-hover">
          <!--Table head-->
          <thead>
            <tr class="text-white">
              <th>#</th>
              <th>Booking ID</th>
              <th>Check In Date</th>
              <th>Check Out Date</th>
              <th>Number of Members</th>
            </tr>
          </thead>
          <!--Table head-->
          <!--Table body-->
          <tbody v-for="booking in bookings" :key="booking.bookingID">
            <tr>
              <th scope="row">
                {{ index+1 }}
              </th>
              <td>
                {{ booking.bookingID }}
              </td>
              <td>
                {{ booking.checkInDate }}
              </td>
              <td>
                {{ booking.checkOutDate }}
              </td>
              <td>
                {{ booking.noOfMembers }}
              </td>
              <td>
                <button class="custom-btn btn-1" @click="goToFeedback()">
                  <span>Feedback</span>
                </button>
              </td>
            </tr>
          </tbody>
          <!--Table body-->
        </table>
        <!--Table-->
      </div>
    </div>
    <hr class="my-4">
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>

    <br><br>
    <br><br><br><br><br><br><br><br><br><br><br><br>
  </div>
</template>

<script>
import axios from 'axios'
const myaxios = axios.create({ baseURL: 'http://localhost:8080' })
export default {
  data () {
    return {
      bookings: [],
      membersList: [],
      singleRoom: 0,
      doubleRoomList: 0
    }
  },
  mounted () {
    // console.log('mounted')
    myaxios
      .get(
        '/dashboard/customer/bookings'
      )
      .then((response) => {
        this.bookings = response.data
      }
      )
      .catch((error) => {
        this.errorMessage = error.message
        console.error('There was an error!', error)
      })
  },
  methods: {
    // getBookings () {
    //   myaxios
    //     .get(
    //       '/dashboard/customer/bookings'
    //     )
    //     .then((response) => {
    //       this.bookings = response.data
    //     }
    //     )
    //     .catch((error) => {
    //       this.errorMessage = error.message
    //       console.error('There was an error!', error)
    //     })
    // },
    goToFeedback () {
      this.$router.push('')
      // feedback page path
    }

  }

}
</script>

<style>
    @import '@/assets/booking/cust_bookings.css';
</style>
