<template>
  <div class="materialContainer">
    <div class="box">
      <div class="title">
        Login
      </div>

      <div class="input">
        <input id="pEmail" type="text" name="pEmail" placeholder="Email">
        <span class="spin" />
      </div>

      <div class="input">
        <input id="password" type="password" name="password" placeholder="Password">
        <span class="spin" />
      </div>

      <div class="button login">
        <button><span>Log In</span> <i class="fa fa-check" /></button>
      </div>

      <a href="" class="pass-forgot">Forgot your password?</a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
    @import url(@/assets/login/login.css);
</style>
