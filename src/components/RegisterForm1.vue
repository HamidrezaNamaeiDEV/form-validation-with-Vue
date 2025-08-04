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
        <a href="#" class="btn mt-4">ثبت نام</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>