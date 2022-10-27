<template>
  <div class="container emp-profile">
    <form method="post">
      <div class="row">
        <div class="col-md-4">
          <div class="profile-img">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS52y5aInsxSm31CvHOFHWujqUx_wWTS9iM6s7BAm21oEN_RiGoog" alt="">
            <div class="file btn btn-lg btn-primary">
              Change Photo
              <input type="file" name="file">
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="profile-head">
            <h5>
              Kshiti Ghelani
            </h5>
            <ul id="myTab" class="nav nav-tabs" role="tablist">
              <li class="nav-item">
                <a
                  id="home-tab"
                  class="nav-link active"
                  data-toggle="tab"
                  href="#home"
                  role="tab"
                  aria-controls="home"
                  aria-selected="true"
                >About</a>
              </li>
              <!-- <li class="nav-item">
                  <a
                    id="profile-tab"
                    class="nav-link"
                    data-toggle="tab"
                    href="#profile"
                    role="tab"
                    aria-controls="profile"
                    aria-selected="false"
                  >Timeline</a>
                </li> -->
            </ul>
          </div>
        </div>
        <div class="col-md-2">
          <input type="submit" class="profile-edit-btn" name="btnAddMore" value="Edit Profile">
        </div>
      </div>
      <div class="row">
        <div class="col-md-4">
          <!-- <div class="profile-work">
              <p>WORK LINK</p>
              <a href="">Website Link</a><br>
              <a href="">Bootsnipp Profile</a><br>
              <a href="">Bootply Profile</a>
              <p>SKILLS</p>
              <a href="">Web Designer</a><br>
              <a href="">Web Developer</a><br>
              <a href="">WordPress</a><br>
              <a href="">WooCommerce</a><br>
              <a href="">PHP, .Net</a><br>
            </div> -->
        </div>
        <div class="col-md-8">
          <div id="myTabContent" class="tab-content profile-tab">
            <div v-for="user in users" :key="user.userID" class="tab-pane fade show active" role="tabpanel" aria-labelledby="home-tab">
              <div class="row">
                <div class="col-md-6">
                  <label>User Id</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.userID }}</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Name</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.fname + user.lname }} </p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Email</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.pEmail }}</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Address</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.houseNo + ","+ user.city + "," + user.state }}</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Country</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.country }}</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Pin Code</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.pinCode }}</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Gender</label>
                </div>
                <div class="col-md-6">
                  <p>{{ user.gender }}</p>
                </div>
              </div>
            </div>
            <div id="profile" class="tab-pane fade" role="tabpanel" aria-labelledby="profile-tab">
              <div class="row">
                <div class="col-md-6">
                  <label>Experience</label>
                </div>
                <div class="col-md-6">
                  <p>Expert</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Hourly Rate</label>
                </div>
                <div class="col-md-6">
                  <p>10$/hr</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Total Projects</label>
                </div>
                <div class="col-md-6">
                  <p>230</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>English Level</label>
                </div>
                <div class="col-md-6">
                  <p>Expert</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-6">
                  <label>Availability</label>
                </div>
                <div class="col-md-6">
                  <p>6 months</p>
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <label>Your Bio</label><br>
                  <p>Your detail description</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
import axios from 'axios'
const myaxios = axios.create({ baseURL: 'http://localhost:8080' })
export default {
  data () {
    return {
      users: []
    }
  },
  mounted () {
    // console.log('mounted')
    myaxios
      .get(
        '/dashboard'
      )
      .then(response => (this.users = response.data))
      .catch((error) => {
        this.errorMessage = error.message
        console.error('There was an error!', error)
      })
  }
}
</script>

  <style>
      @import '@/assets/profile/profile.css';
  </style>
