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
                        Log In
                      </h2>
                    </div>
                  </form>
                  <div class="logIn">
                    <span>
                      <input type="text" class="form" placeholder="Email" autocomplete="off" style="cursor: auto;">
                      <span class="underline" />
                    </span>
                    <span>
                      <input type="password" class="form" placeholder="Password" autocomplete="off" style="cursor: auto;">
                      <span class="underline" />
                    </span>
                  </div>
                  <center class="but-grp">
                    <button class="custom-btn btn-1">
                      <span>Customer Log In</span>
                    </button>
                    <button class="custom-btn btn-1">
                      <span>Employee Log In</span>
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
export default {}
</script>

<style scoped>
    @import url(@/assets/login/login.css);
</style>
