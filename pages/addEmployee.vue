<!-- <template>
  <div>
    <div class="bgImg" />
    <div class="content">
      <div class="d-flex h-100 align-items-center justify-content-center">
        <div class="container">
          <div class="row">
            <div class="col-md-7 col-sm-6 ml-auto mr-auto">
              <div class="card1">
                <div class="card-body">
                  <form>
                    <div class="glowBox">
                      <h2 class="title">
                        Add Employee
                      </h2>
                    </div>
                  </form>
                  <div class="signUp">
                    <span class="req">
                      <input
                        v-model="fname"
                        type="text"
                        class="form"
                        placeholder="First Name"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="lname"
                        type="text"
                        class="form"
                        placeholder="Last Name"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="pEmail"
                        type="text"
                        class="form"
                        placeholder="Email"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="pswd"
                        type="password"
                        class="form"
                        placeholder="Password"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />

                    </span>
                    <h5 class="form-head">
                      <u>Permanent Address</u>
                    </h5>
                    <span>
                      <input
                        v-model="houseNo"
                        type="text"
                        class="form"
                        placeholder="House Number"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="city"
                        type="text"
                        class="form"
                        placeholder="City"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="state"
                        type="text"
                        class="form"
                        placeholder="State"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="country"
                        type="text"
                        class="form"
                        placeholder="Country"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="pinCode"
                        type="text"
                        class="form"
                        placeholder="Pincode"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <h5 class="form-head">
                      <u>Current Address</u>
                    </h5>
                    <span>
                      <input
                        v-model="currHouseNo"
                        type="text"
                        class="form"
                        placeholder="House Number"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="currCity"
                        type="text"
                        class="form"
                        placeholder="City"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="currState"
                        type="text"
                        class="form"
                        placeholder="State"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>

                    <span>
                      <input
                        v-model="currPinCode"
                        type="text"
                        class="form"
                        placeholder="Pincode"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <h5 class="form-head">
                      <u>Other Details</u>
                    </h5>
                    <span>
                      <input
                        v-model="gender"
                        type="text"
                        class="form"
                        placeholder="Gender"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="maritalStatus"
                        type="text"
                        class="form"
                        placeholder="Marital Status"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="panCard"
                        type="text"
                        class="form"
                        placeholder="Pan Card Number"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="accountNo"
                        type="text"
                        class="form"
                        placeholder="Account Number"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="IFSCCode"
                        type="text"
                        class="form"
                        placeholder="IFSC Code"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="bankName"
                        type="text"
                        class="form"
                        placeholder="Bank Name"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                    <span>
                      <input
                        v-model="deptName"
                        type="text"
                        class="form"
                        placeholder="Department Name"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
                  </div>
                  <center>
                    <button class="custom-btn btn-1" @click="addEmp">
                      <span>Add</span>
                    </button>
                  </center>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
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

  <style>
  @import '@/assets/register/register.css';
  @import '@/assets/employee/addEmp.css';

  </style> -->

<template>
  <div>
    <NavBar />
    <div class="container">
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

<style>

  @import '@/assets/employee/addEmp.css'
</style>
