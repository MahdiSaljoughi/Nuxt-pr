<template>
  <Head>
    <Title>ورود / ثبت نام</Title>
  </Head>
  <div
    class="mt-[200px] md:mt-[300px] md:mb-[50px] flex justify-center items-center"
  >
    <img
      src="/public/mobit.svg"
      alt="logo"
      style="margin-bottom: 20px"
      class="w-[140px] md:w-[125px] z-50"
    />
  </div>
  <div
    id="app"
    class="text-center md:shadow-[0px_0px_40px_-10px_rgba(0,0,0,0.2)] w-[400px] mx-auto rounded-[24px] py-5 z-40"
  >
    <Form method="POST" @submit="onSubmit" class="flex flex-col gap-y-5">
      <input
        v-model="username"
        v-bind="usernameAttrs"
        name="username"
        type="text"
        class="user mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="نام کاربری"
      />
      <span>{{ errors.username }}</span>
      <input
        v-model="email"
        v-bind="emailAttrs"
        name="email"
        type="email"
        class="mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="ایمیل"
      />
      <span>{{ errors.email }}</span>
      <input
        v-model="password"
        v-bind="passwordAttrs"
        name="password"
        type="password"
        class="mx-auto outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4"
        placeholder="پسورد"
      />
      <span>{{ errors.password }}</span>
      <button
        type="submit"
        class="mx-auto bg-gray-100 w-[90%] h-[45px] rounded-[16px] text-[12px] font-bold text-gray-400 focus:bg-blue-600 focus:text-white"
      >
        ثبت نام
      </button>
    </Form>
  </div>
  <div>
    <img
      src="/public/mfoter.svg"
      class="fixed bottom-0 w-full md:hidden"
      alt=""
    />
  </div>
</template>

<style scoped>
span {
  color: red;
  /* background-color: rgba(255, 0, 0, 0.102);
  margin-left: 120px;
  margin-right: 120px;
  margin-top: -8px;
  padding: 8px;
  border-radius: 16px; */
  font-size: 12.8px;
}
</style>

<script setup>
import { useForm } from "vee-validate";
import * as yup from "yup";

const schema = yup.object({
  username: yup.string().required(),
  email: yup.string().email().required(),
  password: yup.string().min(8).required(),
});

const { defineField, errors, handleSubmit } = useForm({
  validationSchema: schema,
});

const [username, usernameAttrs] = defineField("username");
const [email, emailAttrs] = defineField("email");
const [password, passwordAttrs] = defineField("password");

const onSubmit = handleSubmit((values) => {
  alert(JSON.stringify(values, null, 2));
});
</script>