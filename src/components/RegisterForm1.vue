<template>
  <div class="card-back">
    <div class="center-wrap">
      <form @submit.prevent="register" class="section text-center">
        <h4 class="mb-4 pb-3">ثبت نام</h4>
        <div class="form-group">
          <input
            v-model="name"
            type="text"
            class="form-style"
            placeholder="نام و نام خانوادگی"
            autocomplete="off"
          />
          <i class="input-icon uil uil-user"></i>
        </div>
        <div class="form-group mt-2">
          <input
            v-model="email"
            type="email"
            class="form-style"
            placeholder="ایمیل خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-at"></i>
        </div>
        <div class="form-group mt-2">
          <input
            v-model="password"
            type="password"
            class="form-style"
            placeholder="کلمه عبور"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <div class="form-group mt-2">
          <input
            v-model="ConfirmPassword"
            type="password"
            class="form-style"
            placeholder="تکرار کلمه عبور"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <div class="form-group mt-2">
          <input
            v-model="phoneNumber"
            type="text"
            class="form-style"
            placeholder="شماره خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-phone"></i>
        </div>

        <div class="form-group mt-2">
        <select v-model="role" class="form-style">
          <option value="">نقش خود را وارد کنید</option>
          <option value="کاربر">کاربر</option>
          <option value="مدرس">مدرس</option>
          <option value="مدیر">مدیر</option>
        </select>
        <i class="input-icon uli uil-airplay"></i>
        </div>
        
        <div class="form-group d-flex mt-2 ms-2 text-start">
          <label for="1">نامشخص</label>
          <input v-model="gender" type="radio" name="gender" value="نامشخص" id="1" class="m-1">

          <label for="2">آقا</label>
          <input v-model="gender" type="radio" name="gender" value="آقا" id="2" class="m-1">
        
          <label for="3">خانم</label>
          <input v-model="gender" type="radio" name="gender" value="خانم" id="3" class="m-1">
        </div>

        <button class="btn mt-4">ثبت نام</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name : "",
      email : "",
      phoneNumber : "",
      password : "",
      ConfirmPassword : "",
      gender : "نامشخص",
      role : "کاربر",
    };
  },
  methods:{
    register(){
      console.log(this.name);
      console.log(this.email);
      console.log(this.phoneNumber);
      console.log(this.password);
      console.log(this.ConfirmPassword);
      console.log(this.gender);
      console.log(this.role);
    }
  }
};
</script>

<style>
</style>