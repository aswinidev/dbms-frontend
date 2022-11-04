<template>
  <center>
    <div class="col-md-6 col-sm-6 ">
      <div class="chunk booking-card clearfix">
        <div class="row">
          <div class="col-md-3 col-sm-3 col-xs-3">
            <span class="profile-pic" />
          </div>
          <div class="col-md-9 col-sm-9 col-xs-9 name-date">
            <div class="guest-name">
              {{ booking.bookingID }}
            </div>
          </div>
        </div>
        <div class="row card-row">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="check-in">
              Check In Date
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="check-in-date">
              {{ booking.checkInDate }}
            </span>
          </div>
        </div>
        <div class="row card-row">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="check-out">
              Check Out Date
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="check-out-date">
              {{ booking.checkOutDate }}
            </span>
          </div>
        </div>
        <div class="row card-row">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="Details">
              Number Of Members
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="nights">
              {{ booking.noOfMembers }}
            </span>
          </div>
        </div>
        <div class="row card-row">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="Details">
              Number Of Single Rooms
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="nights">
              {{ singleRooms }}
            </span>
          </div>
        </div>
        <div class="row card-row">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="Details">
              Number Of Double Rooms
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="nights">
              {{ doubleRooms }}
            </span>
          </div>
        </div>

        <div class="row card-row total">
          <div class="col-md-3 col-sm-3 col-xs-4 card-catergory">
            <span class="earnings">
              Total Price
            </span>
          </div>
          <div class="col-md-9 col-sm-9 col-xs-8 card-data">
            <span class="earnings-total">
              {{ booking.price }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </center>
</template>

<script>
import axios from 'axios'
const myaxios = axios.create({ baseURL: 'http://localhost:8080' })
export default {
  data () {
    return {
      props: ['id'],
      booking: {}
    }
  },
  mounted () {
    // getmapping for the passed bookingID
    myaxios
      .post(
        '/', { bookingID: this.id }
        // get mapping for given booking
      )
      .then((response) => {
        this.booking = response.data
      }
      )
      .catch((error) => {
        this.errorMessage = error.message
        console.error('There was an error!', error)
      })
  }

}
</script>

<style>
@import "@/assets/booking/bookingDetails.css"
</style>
