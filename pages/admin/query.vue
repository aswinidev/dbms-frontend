<template>
  <div>
    <NavBar />
    <div v-if="getDetails===false" style="height: 100vh">
      <div class="row justify-content-between" style="text-align:center; margin-top: 40px">
        <div class="col-4">
          <h1>Customer Queries</h1>
        </div>
      </div>
      <!-- <QueryList /> -->
      <QueryList
        v-for="query in queries"
        :key="query.queryID"
        :name="query.name"
        :query="query.query"
        :emailid="query.emailID"
        @clicked="onClickListItem(query)"
      />
    </div>
    <div v-else>
      <button class="custom-btn btn-1" @click="goBacktoPage">
        <span>Back</span>
      </button>
      <ReplyQuery :query="query" />
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
      getDetails: false,
      queries: [],
      query: {}
    }
  },
  mounted () {
    this.landingRequest()
  },
  methods: {
    landingRequest () {
      myaxios
        .get(
          '/admin/allQuery',
          {
            headers: {
              Authorization: `Bearer ${localStorage.getItem('token')}`
            }
          }

        )
        .then((response) => {
          this.queries = response.data
          console.log(JSON.stringify(this.queries))
        }
        )
        .catch((error) => {
          this.errorMessage = error.message
          console.error('There was an error!', error)
        })
    },
    onClickListItem (value) {
      this.getDetails = true
      this.query = value
    },
    goBacktoPage () {
      this.landingRequest()
      this.getDetails = false
    }
  }

}
</script>

<style scoped>
    @import '@/assets/booking/bookingList.css'
</style>
