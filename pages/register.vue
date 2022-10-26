<template>
  <div>
    <div class="bgImg" />
    <div class="content">
      <div class="d-flex h-100 align-items-center justify-content-center">
        <div class="container">
          <div class="row">
            <div class="col-md-7 col-sm-6 ml-auto mr-auto">
              <div class="card">
                <div class="card-body">
                  <form>
                    <div class="glowBox">
                      <h2 class="title">
                        Sign Up
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
                        v-model="password"
                        type="password"
                        class="form"
                        placeholder="Password"
                        autocomplete="off"
                        style="cursor: auto;"
                      >
                      <span class="underline" />
                    </span>
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
                      <input v-model="fname" type="number" class="form" placeholder="Number of Members" autocomplete="off" style="cursor: auto;">
                      <span class="underline" />
                    </span>
                    <span>
                      <input v-model="fname" type="text" class="form" placeholder="Aadhar Card Number" autocomplete="off" style="cursor: auto;">
                      <span class="underline" />
                    </span>
                    <span>
                      <input v-model="fname" type="text" class="form" placeholder="Alternate Email Address" autocomplete="off" style="cursor: auto;">
                      <span class="underline" />
                    </span>
                  </div>
                  <center>
                    <button class="custom-btn btn-1" @click="register">
                      <span>Sign Up</span>
                    </button>
                  </center>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Axios from 'axios'
export default {
  data () {
    return {
      fname: '',
      lname: '',
      pEmail: '',
      password: '',
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
      Axios('http://localhost:8081/register')
      Axios.post('http://localhost:8081/register', {
        name: this.fname,
        password: this.password
      }).then(function (response) {
        console.log(this.fname)
      })
    }
  }
}
</script>

<style>
@import '@/assets/register/register.css';

</style>
