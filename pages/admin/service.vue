<template>
  <div>
    <NavBar />
    <div v-if="getDetails===false" style="min-height: 100vh">
      <div class="row justify-content-between" style="text-align:center; margin-top: 40px">
        <div class="col-4">
          <h1>Services Available</h1>
        </div>
        <div class="col-4">
          <b-button size="lg" variant="dark" href="/serviceForm">
            Add Service
          </b-button>
        </div>
      </div>
      <ServiceList
        v-for="service in services"
        :key="service.serviceName"
        :sname="service.serviceName"
        :availability="service.availability"
        :price="service.price"
        :headedby="service.headedBy"
      />
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
      services: [],
      getDetails: false
    }
  },
  mounted () {
    // getmapping
    myaxios
      .get(
        '/admin/service', // get mapping for all bookings
        {
          headers: {
            // Authorization: 'Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJMS05GTE4iLCJpYXQiOjE2NjcwNDkwNTQsImV4cCI6MTY2NzA1OTg1NH0.GdsK7YclD7Eeg6UJU2h8femd4FvPe1TOl8zbwm6iNd_gZejtH45Mo1YP8XIzdDrKbVA_7YshzZKHcbr3Dbw_1Q'
            Authorization: `Bearer ${localStorage.getItem('token')}`
          }
        }

      )
      .then((response) => {
        this.services = response.data
        console.log(JSON.stringify(this.services))
      }
      )
      .catch((error) => {
        this.errorMessage = error.message
        console.error('There was an error!', error)
      })
  },
  methods: {
    onClickListItem (value) {
      this.getDetails = true
      this.booking = value
      console.log(this.id)
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
