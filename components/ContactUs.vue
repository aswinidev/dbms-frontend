<template>
  <div>
    <div class="container">
      <form class="form-container">
        <div class="headline">
          <span>Contact Us</span>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey;">Name</label><br><br>
          <input v-model="name" type="text" class="form-input" required>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Contact Number</label><br><br>
          <input v-model="contactNumber" type="" class="form-input" required>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Email</label><br><br>
          <input v-model="emailID" type="Email" class="form-input" required>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Query</label><br><br>
          <textarea v-model="query" class="form-input" required rows="10" />
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
      name: '',
      contactNumber: '',
      query: '',
      emailID: ''
    }
  },
  methods: {
    sendQuery () {
      myaxios
        .post('/contactus',
          {
            name: this.name,
            contactNumber: this.contactNumber,
            query: this.query,
            emailID: this.emailID
          },
          {
            headers: {
            // Authorization: 'Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJMS05GTE4iLCJpYXQiOjE2NjcwNDkwNTQsImV4cCI6MTY2NzA1OTg1NH0.GdsK7YclD7Eeg6UJU2h8femd4FvPe1TOl8zbwm6iNd_gZejtH45Mo1YP8XIzdDrKbVA_7YshzZKHcbr3Dbw_1Q'
              Authorization: `Bearer ${localStorage.getItem('token')}`
            }
          }
        )
        .then(function (response) {
          console.log(response.data)
        })
        .catch((error) => {
          this.errorMessage = error.message
          console.error('There was an error!', error)
        })
    }
  }
}
</script>

<style scoped>
  @import '@/assets/contactus/contactus.css'
  </style>
