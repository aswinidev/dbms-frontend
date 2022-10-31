
<template>
  <div id="booking" class="section">
    <div class="section-center">
      <div class="container">
        <div class="row">
          <div class="booking-form">
            <div class="form-header">
              <h1>Make your reservation</h1>
            </div>
            <form>
              <!-- <div class="form-group">
                <input class="form-control" type="text" placeholder="Country, ZIP, city...">
                <span class="form-label">Destination</span>
              </div>  -->
              <div class="row">
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control" type="date" required>
                    <span class="form-label">Check In</span>
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control" type="date" required>
                    <span class="form-label">Check out</span>
                  </div>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control" type="number" placeholder="No of Single rooms" min="0" required>
                    <span class="form-label">No of Single rooms</span>
                  <!-- <select class="form-control" required>
                    <option value="" selected hidden>
                      no of rooms
                    </option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                  </select>
                  <span class="select-arrow" />
                  <span class="form-label">Rooms</span>  -->
                  </div>
                </div>
                <div class="col-md-6">
                  <div class="form-group">
                    <input class="form-control" type="number" placeholder="No of Double rooms" min="0" required>
                    <span class="form-label">No of Double rooms</span>
                  <!-- <select class="form-control" required>
                    <option value="" selected hidden>
                      no of adults
                    </option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                  </select>
                  <span class="select-arrow" />
                  <span class="form-label">Adults</span> -->
                  </div>
                </div>
              <!-- <div class="col-md-4">
                <div class="form-group">
                  <select class="form-control" required>
                    <option value="" selected hidden>
                      no of children
                    </option>
                    <option>0</option>
                    <option>1</option>
                    <option>2</option>
                  </select>
                  <span class="select-arrow" />
                  <span class="form-label">Children</span>
                </div>
              </div> -->
              </div>
              <!-- <div class="row">
              <div class="col-md-6">
                <div class="form-group">
                  <input class="form-control" type="email" placeholder="Enter your Email">
                  <span class="form-label">Email</span>
                </div>
              </div>
              <div class="col-md-6">
                <div class="form-group">
                  <input class="form-control" type="tel" placeholder="Enter you Phone">
                  <span class="form-label">Phone</span>
                </div>
              </div>
            </div> -->
              <div class="form-btn">
                <button class="submit-btn">
                  Check Availability
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- <a target="_blank" href="https://gosnippets.com" class="white-mode">MORE</a> -->
</template>

<script>
import axios from 'axios'
const myaxios = axios.create({ baseURL: 'http://localhost:8080' })
export default {
  data () {
    return {
      fname: '',
      lname: '',
      pEmail: '',
      pswd: '',
      houseNo: '',
      state: '',
      city: '',
      country: '',
      pinCode: '',
      gender: ''
    }
  },
  methods: {
    register () {
      myaxios.post('/register', {
        fname: this.fname,
        lname: this.lname,
        pEmail: this.pEmail,
        pswd: this.pswd,
        houseNo: this.houseNo,
        state: this.state,
        city: this.city,
        country: this.country,
        pinCode: this.pinCode,
        gender: this.gender
      }).then(function (response) {
        console.log(response.data)
      })
    }
  }
}
</script>

<style scoped>
    @import '@/assets/booking/booking-form.css';
</style>
