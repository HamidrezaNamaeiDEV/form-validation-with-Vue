<template>
  <div class="card-back">
    <div class="center-wrap">
      <Form @submit="register" class="section text-center" :validation-schema="RegisterFormSchema" :initial-values="formData">
        <h4 class="mb-4 pb-3">ثبت نام</h4>
        <div class="form-group">
          <Field
            :validateOnInput="true"
            name="name"
            type="text"
            class="form-style"
            placeholder="نام و نام خانوادگی"
            autocomplete="off"
          />
          <i class="input-icon uil uil-user"></i>
        </div>
        <p class="text-danger">
          <ErrorMessage name="name" />
        </p>
        <div class="form-group mt-2">
          <Field
            :validateOnInput="true"
            name="email"
            type="email"
            class="form-style"
            placeholder="ایمیل خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-at"></i>
        </div>
        <p  class="text-danger">
          <ErrorMessage name="email" />
        </p>
        <div class="form-group mt-2">
          <Field
            :validateOnInput="true"
            name="password"
            type="password"
            class="form-style"
            placeholder="کلمه عبور"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <p  class="text-danger">
          <ErrorMessage name="password" />
        </p>
        <div class="form-group mt-2">
          <Field
            :validateOnInput="true"
            name="ConfirmPassword"
            type="password"
            class="form-style"
            placeholder="تکرار کلمه عبور"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <p  class="text-danger">
          <ErrorMessage name="ConfirmPassword" />
        </p>
        <div class="form-group mt-2">
          <Field
            :validateOnInput="true"
            name="phoneNumber"
            type="text"
            class="form-style"
            placeholder="شماره خود را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-phone"></i>
        </div>
        <p  class="text-danger">
          <ErrorMessage name= "phoneNumber" />
        </p>
        <div class="form-group mt-2">
        <Field :validateOnInput="true" as="select" name="role" class="form-style">
          <option value="">نقش خود را وارد کنید</option>
          <option value="کاربر">کاربر</option>
          <option value="مدرس">مدرس</option>
          <option value="مدیر">مدیر</option>
        </Field>
        <i class="input-icon uli uil-airplay"></i>
        </div>
        <p  class="text-danger">
          <ErrorMessage name= "role" />
        </p>
        
        <div class="form-group d-flex mt-2 ms-2 text-start">
          <label for="1">نامشخص</label>
          <Field v-model="gender" type="radio" name="gender" value="نامشخص" id="1" class="m-1" />

          <label for="2">آقا</label>
          <Field v-model="gender" type="radio" name="gender" value="آقا" id="2" class="m-1" />
        
          <label for="3">خانم</label>
          <Field v-model="gender" type="radio" name="gender" value="خانم" id="3" class="m-1" />
        </div>
        <button class="btn mt-4">ثبت نام</button>
      </form>
    </div>
  </div>
</template>

<script>
import { Form, Field, ErrorMessage} from "vee-validate";
import {string,object ,ref} from 'yup';
export default {
  data() {
    const RegisterFormSchema = object({
      name : string().required("لطفا نام را وارد کنید"),
      email : string().required("ایمیل را وارد کنید").email("ایمیل نامعتبر است"),
      password : string().required("لطفا رمز عبور را وارد کنید").min(6,"لطفا رمز عبور با بیش از 5 کاراکتر انتخاب کنید"),
      ConfirmPassword : string().required("لطفا رمز عبور را تایید کنید").oneOf([ref("password")],"رمز های عبور یکسان نیستند"),
      phoneNumber : string().required("لطفا شماره تلفن را وراد کنید").length(11),
      role: string().required("لطفا نقش خود را انتخاب کنید"),
    })
    return {
      RegisterFormSchema,
      formData:{
        gender: "نامشخص",
        role : "کاربر",
      }
    };
  },
  components:{
    Form,Field,ErrorMessage
  },
  methods:{
    // register(){
    //   this.validateProperties();
    //   if(this.isOk){
    //       console.log(this.name);
    //       console.log(this.email);
    //       console.log(this.phoneNumber);
    //       console.log(this.password);
    //       console.log(this.ConfirmPassword);
    //       console.log(this.gender);
    //       console.log(this.role);
    //   }
    // },
    // validateProperties(){
    //   if(validateEmail(this.email) == false){
    //     this.$toast.error("ایمیل نامعتبر میباشد")
    //   }else if(this.phoneNumber.length != 11){
    //     this.$toast.error("شماره تلفن معتبر نمیباشد")
    //   }
    //   else if(!this.name){
    //     this.$toast.error("لطفا نام را وارد کنید")
    //   }
    //   else if(!this.phoneNumber){
    //     this.$toast.error("لطفا شماره تلفن را وراد کنید")
    //   }
    //   else if(!this.role){
    //     this.$toast.error("لطفا نقش خود را انتخاب کنید")
    //   }
    //   else if(!this.password){
    //     this.$toast.error("لطفا رمز عبور مناسبی بنویسید")
    //   }
    //   else if(this.ConfirmPassword !=this.password){
    //     this.$toast.error("لطفا رمز عبور را تایید کنید")
    //   }
    //   else{
    //     this.isOk = true;
    //   }
    // }
  }
  
}
</script>

<style>
</style>