<template>
  <section>
    <div class="container">
      <!-- <h1 style="text-align: center; margin-bottom: 40px;">
        Employee List
      </h1> -->
      <div class="request-details">
        <div class="company">
          <div class="placeholder">
            <i class="fas fa-building" />
            <p>Employee ID</p>
          </div>
          <h3>{{ bookingid }}</h3>
        </div>
        <div class="company">
          <div class="placeholder">
            <i class="fas fa-building" />
            <p>First Name</p>
          </div>
          <h3>{{ checkin }}</h3>
        </div>
        <div class="company">
          <div class="placeholder">
            <i class="fas fa-building" />
            <p>Last Name</p>
          </div>
          <h3>{{ checkout }}</h3>
        </div>
        <div class="company">
          <div class="placeholder">
            <i class="fas fa-building" />
            <p>Department Name</p>
          </div>
          <h3>{{ checkout }}</h3>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      props: ['bookingid', 'checkin', 'checkout']
    }
  },
  methods: {
    goToDetails (event) {
      this.$emit('clicked')
    }
  }
}
</script>

  <style scoped>
  @import '@/assets/booking/bookingList.css'
  </style>
