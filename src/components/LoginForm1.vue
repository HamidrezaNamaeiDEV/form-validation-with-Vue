<template>
  <div class="card-front">
    <div class="center-wrap">
      <Form @submit="login" class="section text-center" :validation-schema="loginFormSchema">
        <h4 class="mb-4 pb-3">ورود</h4>
        <div class="form-group">
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
        <p class="text-danger">
            <ErrorMessage name="email" />
        </p>
        <div class="form-group mt-2">
          <Field
            :validateOnInput="true"
            name="password"
            type="password"
            class="form-style"
            placeholder="پسورد را وارد کنید"
            autocomplete="off"
          />
          <i class="input-icon uil uil-lock-alt"></i>
        </div>
        <p class="text-danger">
          <ErrorMessage name="password" />
        </p>
        <button class="btn mt-4">ورود به سایت</button>
        <p class="mb-0 mt-4 text-center">
          <a href="#0" class="link">آیا کلمه عبور خود را فراموش کرده اید ؟</a>
        </p>
      </Form>
    </div>
  </div>
</template>

<script>
import { Form, Field, ErrorMessage} from "vee-validate";
import * as yup from 'yup';

export default {
  name: "LoginForm",
  components:{
    Form,
    Field,
    ErrorMessage,
  },
  data(){
    // validate with yup schema
    const loginFormSchema = yup.object({
      email : yup.string().required("ایمیل را وارد کنید").email("ایمیل نامعتبر است"),
      password : yup.string().required("لطفا رمز عبور را وارد کنید").min(5,"لطفا رمز عبور با بیش از 5 کاراکتر انتخاب کنید")
    })
    return{
      // validate with yup
      // emailRule:yup.string().required("ایمیل را وارد کنید").email("ایمیل نامعتبر است"),
      // passwordRule:yup.string().required("لطفا رمز عبور را وارد کنید").min(5,"لطفا رمز عبور با بیش از 5 کاراکتر انتخاب کنید")
      
      loginFormSchema
    }
  },
  methods:{
    login(values){
      console.log(values)
    },
    // old way
    // validateEmail(email) {
    //   if (!email) {
    //     return "لطفا ایمیل را وارد کنید"
    //   }
    //   const regex = /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}$/i;
    //   if (!regex.test(email)) {
    //     return 'ایمیل نا معتبر است';
    //   }
    //   return true;
    // },
    // validatePassword(password){
    //   if (!password) {
    //     return "لطفا رمز عبور را وارد کنید"
    //   }
    //   if (password.length <= 5) {
    //     return "لطفا رمز عبور با بیش از 5 کاراکتر انتخاب کنید"
    //   }
      
    //   return true;
    // }

  }
};
</script>

<style>
</style>