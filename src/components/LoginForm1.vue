<template>
  <div class="card-front">
    <div class="center-wrap">
      <form @submit.prevent="login" class="section text-center">
        <h4 class="mb-4 pb-3">ورود</h4>
        <div class="form-group">
          <input
            v-model="email"
            type="email"
            name="logemail"
            class="form-style"
            placeholder="ایمیل خود را وارد کنید"
            id="logemail"
            autocomplete="off"
          />
          <i class="input-icon uil uil-at"></i>
        </div>
        <div class="form-group mt-2">
          <input
            v-model="password"
            type="password"
            name="logpass"
            class="form-style"
            placeholder="پسورد را وارد کنید"
            id="logpass"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <button class="btn mt-4">ورود به سایت</button>
        <p class="mb-0 mt-4 text-center">
          <a href="#0" class="link">آیا کلمه عبور خود را فراموش کرده اید ؟</a>
        </p>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginForm",
  data(){
    return{
      email:"",
      password:"",
    }
  },
  methods:{
    login(){
      console.log(this.email);
      console.log(this.password);
    }
  }
};
</script>

<style>
</style>