<template>
  <Head>
    <Title>ورود / ثبت نام</Title>
  </Head>
  <div>
    <div class="mt-[250px] md:mt-[300px] md:mb-[50px] flex justify-center items-center">
        <img src="/mobit.svg" alt="" class="w-[140px] md:w-[125px]">
    </div>
    <div class="text-center md:shadow-[0px_0px_40px_-10px_rgba(0,0,0,0.2)] w-[400px] mx-auto
    rounded-[24px] py-5">
      <form action="/" method="POST" class="flex flex-col gap-y-5">
        <div class="flex items-center justify-start pr-6 pt-2">
            <span class="text-xl font-bold tracking-tight">ورود به مبیت</span>
        </div>
        <div>
          <input :rules="isRequired" class="outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4" type="text" name="username" placeholder="نام کاربری" />
        </div>
        <div>
          <input class="outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4" type="email" name="email" placeholder="ایمیل" />
        </div>
        <div>
          <input class="outline-none focus:ring-2 ring-blue-500 bg-gray-100 w-[90%] h-[45px] rounded-[16px] placeholder:text-[12px] px-4" type="password" name="password" placeholder="پسورد" />
        </div>
        <span class="bg-gray-200 w-[80%] h-[2px] mx-auto my-2"></span>
        <div>
          <button type="submit" class="bg-gray-100 w-[90%] h-[45px] rounded-[16px] font-bold text-gray-400 focus:bg-blue-600 focus:text-white">ورود</button>
        </div>
      </form>
    </div>
    <div>
        <img src="/mfoter.svg" class="fixed bottom-0 w-full md:hidden" alt="">
    </div>
  </div>
</template>

<script setup>

</script>