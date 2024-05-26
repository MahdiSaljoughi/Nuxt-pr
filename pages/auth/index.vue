<template>
  <Head>
    <Title>ورود / ثبت نام</Title>
  </Head>
  <div
    class="mt-[250px] md:mt-[300px] md:mb-[50px] flex justify-center items-center"
  >
    <img src="/public/mobit.svg" alt="logo" style="margin-bottom: 20px;" class="w-[140px] md:w-[125px] z-50" />
  </div>
  <div
    id="app"
    class="text-center md:shadow-[0px_0px_40px_-10px_rgba(0,0,0,0.2)] w-[400px] mx-auto rounded-[24px] py-5 z-40"
  >
    <Form action="/" method="POST" class="flex flex-col gap-y-5">
      <Field
        name="username"
        type="text"
        :rules="validateUserName"
        class="mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="نام کاربری"
      />
      <ErrorMessage name="username" />
      <Field
        name="email"
        type="email"
        :rules="validateEmail"
        class="mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="ایمیل"
      />
      <ErrorMessage name="email" />
      <Field
        name="password"
        type="password"
        :rules="validatePassword"
        class="mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="پسورد"
      />
      <ErrorMessage name="password" />
      <button type="submit"
        class="mx-auto bg-gray-100 w-[90%] h-[45px] rounded-[16px] text-[12px] font-bold text-gray-400 focus:bg-blue-600 focus:text-white"
      >
        ثبت نام
      </button>
    </Form>
  </div>
  <div>
    <img src="/public/mfoter.svg" class="fixed bottom-0 w-full md:hidden" alt="" />
  </div>
</template>
<style scoped>
span {
  color: red;
  background-color: rgba(255, 0, 0, 0.102);
  margin-left: 120px;
  margin-right: 120px;
  margin-top: -8px;
  padding: 8px;
  font-size: 12.8px;
  border-radius: 16px;
}
</style>
<script>
import { Form, Field, ErrorMessage } from "vee-validate";
export default {
  components: {
    Form,
    Field,
    ErrorMessage,
  },
  methods: {
    validateUserName(value) {
      if (!value) {
        return "این فیلد الزامی می باشد !";
      }
      const regex = /^[a-z]{3,10}/;
      if (!regex.test(value)) {
        return "نام کاربری معتبر نیست !";
      }
      return true;
    },
    validateEmail(value) {
      if (!value) {
        return "این فیلد الزامی می باشد !";
      }
      const regex = /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}$/i;
      if (!regex.test(value)) {
        return "ایمیل اشتباه است !";
      }
      return true;
    },
    validatePassword(value) {
      if (!value) {
        return "این فیلد الزامی می باشد !";
      }
      const regex = /^[a-zA-Z0-9]{8,50}/;
      if (!regex.test(value)) {
        return "پسورد کوتاه است";
      }
      return true;
    },
  },
};
</script>