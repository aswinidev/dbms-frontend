<template>
  <div>
    <NavBar />
    <div class="ctr">
      <form class="form-container">
        <div class="headline">
          <span>Add Employee</span>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey;">First Name</label><br><br>
          <input
            v-model="fname"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Last Name</label><br><br>
          <input
            v-model="lname"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Email</label><br><br>
          <input
            v-model="pEmail"
            type="Email"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Password</label><br><br>
          <input
            v-model="pswd"
            type="password"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>

        <div class="form-line">
          <label style="font-size: 24px; color: black">Permanent Address</label><br><br>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">House Number</label><br><br>
          <input
            v-model="houseNo"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">City</label><br><br>
          <input
            v-model="city"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">State</label><br><br>
          <input
            v-model="state"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Country</label><br><br>
          <input
            v-model="country"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Pincode</label><br><br>
          <input
            v-model="pinCode"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>

        <div class="form-line">
          <label style="font-size: 24px; color: black">Current Address</label><br><br>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">House Number</label><br><br>
          <input
            v-model="currHouseNo"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">City</label><br><br>
          <input
            v-model="currCity"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">State</label><br><br>
          <input
            v-model="currState"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>

        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Pincode</label><br><br>
          <input
            v-model="pinCode"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 24px; color: black">Other Details</label><br><br>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Gender</label><br><br>
          <input
            v-model="gender"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Marital Status</label><br><br>
          <input
            v-model="maritalStatus"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Pan Card Number</label><br><br>
          <input
            v-model="panCard"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Account Number</label><br><br>
          <input
            v-model="accountNo"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">IFSC Code</label><br><br>
          <input
            v-model="IFSCCode"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Bank Name</label><br><br>
          <input
            v-model="bankName"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Department Name</label><br><br>
          <input
            v-model="deptName "
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>

        <input type="button" class="form-button" value="Submit" style="font-size: 18px;" @click="sendQuery">
      </form>
    </div>
    <Footer />
  </div>
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
      currHouseNo: '',
      currState: '',
      currCity: '',
      currPinCode: '',
      gender: '',
      maritalStatus: '',
      panCard: '',
      accountNo: '',
      IFSCCode: '',
      bankName: '',
      deptName: ''
    }
  },
  methods: {
    addEmp () {
      myaxios.post('/', {
        fname: this.fname,
        lname: this.lname,
        pEmail: this.pEmail,
        pswd: this.pswd,
        houseNo: this.houseNo,
        state: this.state,
        city: this.city,
        country: this.country,
        pinCode: this.pinCode,
        currHouseNo: this.houseNo,
        currState: this.state,
        currCity: this.city,
        currPinCode: this.pinCode,
        gender: this.gender,
        maritalStatus: this.maritalStatus,
        panCard: this.panCard,
        accountNo: this.accountNo,
        IFSCCode: this.IFSCCode,
        bankName: this.bankName,
        deptName: this.deptName
      }).then(function (response) {
        console.log(response.data)
      })
    }
  }
}
</script>

<style scoped>
  @import '@/assets/employee/addEmp.css'
</style>
