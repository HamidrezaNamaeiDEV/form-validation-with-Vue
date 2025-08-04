<template>
  <div class="card-back">
    <div class="center-wrap">
      <div class="section text-center">
        <h4 class="mb-4 pb-3">ثبت نام</h4>
        <div class="form-group">
          <input
            type="text"
            name="logname"
            class="form-style"
            placeholder="نام و نام خانوادگی"
            id="logname"
            autocomplete="off"
          />
          <i class="input-icon uil uil-user"></i>
        </div>
        <div class="form-group mt-2">
          <input
            type="email"
            class="form-style"
            placeholder="ایمیل خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-at"></i>
        </div>
        <div class="form-group mt-2">
          <input
            type="password"
            name="logpass"
            class="form-style"
            placeholder="کلمه عبور"
            id="logpass"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <div class="form-group mt-2">
          <input
            type="password"
            class="form-style"
            placeholder="تکرار کلمه عبور"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <div class="form-group mt-2">
          <input
            type="text"
            class="form-style"
            placeholder="شماره خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-phone"></i>
        </div>

        <div class="form-group mt-2">
        <select name="" id="" class="form-style">
          <option value="">نقش خود را وارد کنید</option>
          <option value="">کاربر</option>
          <option value="">مدرس</option>
          <option value="">مدیر</option>
        </select>
        <i class="input-icon uli uil-airplay"></i>
        </div>
        
        <div class="form-group d-flex mt-2 ms-2 text-start">
          <label for="1">نامشخص</label>
          <input type="radio" name="gender" value="نامشخص" id="1" class="m-1">

          <label for="2">آقا</label>
          <input type="radio" name="gender" value="آقا" id="2" class="m-1">
        
          <label for="3">خانم</label>
          <input type="radio" name="gender" value="خانم" id="3" class="m-1">
        </div>

        <a href="#" class="btn mt-4">ثبت نام</a>
      </div>
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
      gender : "",
      role : "",

    }
  },
};
</script>

<style>
</style>