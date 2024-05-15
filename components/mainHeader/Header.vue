<template>
  <div>
    <!-- Header Tablet & Desktop -->
    <header
      class="hidden lg:block bg-[#1C39BB] px-1.5 w-full fixed text-white shadow-md xl:text-[12.8px] lg:text-[11px] z-50"
    >
      <div class="flex lg:justify-between items-center">
        <div class="items-center lg:mx-0 hidden lg:flex">
          <NuxtLink to="/">
            <div class="2xl:ml-10 xl:ml-7 lg:ml-5 flex items-center">
              <img
                src="~/assets/images/LogoType.png"
                class="2xl:w-[94px] xl:w-[70px] lg:w-[50px] w-20"
                alt="Logo"
              />
            </div>
          </NuxtLink>
          <div class="hidden lg:block">
            <div
              class="flex items-center 2xl:gap-x-8 xl:gap-x-5 lg:gap-x-4 xl:ml-16 lg:ml-8"
            >
              <div class="group/menu py-6">
                <div>
                  <div
                    class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1 cursor-pointer"
                  >
                    <span>
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                        viewBox="0 0 24 24"
                      >
                        <path
                          fill="currentColor"
                          d="M14.116 20q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0-8.5q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14T14.115 4h4.27q.666 0 1.14.475T20 5.615v4.27q0 .666-.475 1.14t-1.14.475zm-8.5 0q-.667 0-1.141-.475T4 9.885v-4.27q0-.666.475-1.14T5.615 4h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0 8.5q-.667 0-1.141-.475T4 18.386v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14T9.885 20z"
                        />
                      </svg>
                    </span>
                    <span class="block">دسته بندی ها</span>
                    <span
                      class="bg-white w-0 lg:group-hover/menu:w-[80px] xl:group-hover/menu:w-[95px] 2xl:group-hover/menu:w-[105px] rounded-full h-[3px] transition-all ease-linear block absolute bottom-1"
                    ></span>
                  </div>
                </div>
                <!-- megeMenu DATA -->
                <div
                  class="relative hidden group-hover/menu:block transition-all"
                >
                  <div
                    class="bg-white w-[240px] h-[388px] text-[#3F434D] text-[13px] absolute top-6 py-3 rounded-br-xl shadow-md transition-all duration-1000"
                  >
                    <!-- 1 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataMobile_1"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[512px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pl-10 pr-3"
                      >
                        <div class="grid grid-cols-2 py-2 pr-2">
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 2 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataJanebi_2"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[512px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pl-10 pr-3"
                      >
                        <div class="grid grid-cols-2">
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 3 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataLaptop_3"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[768px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pl-10 pr-3"
                      >
                        <div class="grid grid-cols-3">
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 4 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataGajet_4"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[256px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pr-3"
                      >
                        <div>
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 5 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataSoti_5"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[256px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pr-3"
                      >
                        <div>
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 6 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataMashin_6"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[256px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pr-3"
                      >
                        <div>
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                    <!-- 7 -->
                    <div
                      v-for="(data, index) in dataMegaMenu.dataConsole_7"
                      :key="index"
                      class="flex items-center gap-x-2 group/list hover:border-t-[1px] px-3 py-1.5 hover:border-b-[1px] border-zinc-700/10 hover:bg-gray-50 hover:text-[#377DFF]"
                    >
                      <img :src="data.img" alt="img" class="w-10" />
                      <a :href="data.link">{{ data.title }}</a>
                      <div
                        class="hidden group-hover/list:block cursor-default bg-white w-[256px] h-[388px] absolute top-0 mr-[228px] rounded-bl-xl shadow-md py-3 pr-3"
                      >
                        <div>
                          <div
                            v-for="(dataChild, index) in data.child"
                            :key="index"
                          >
                            <a
                              :href="dataChild.link"
                              :class="{ borderR: dataChild.BIF }"
                              class="inline-block hover:text-[#377DFF] text-[#3F434D] text-[12px] mb-3"
                              >{{ dataChild.title }}</a
                            >
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- END -->
              </div>
              <nuxt-link to="/shop">
                <div
                  class="group/under flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
                >
                  <span>
                    <svg
                      class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 -960 960 960"
                      fill="#e8eaed"
                    >
                      <path
                        d="M197.83-84.65q-47.96 0-80.57-32.61-32.61-32.61-32.61-80.57v-564.34q0-47.96 32.61-80.57 32.61-32.61 80.57-32.61h564.34q47.96 0 80.57 32.61 32.61 32.61 32.61 80.57v564.34q0 47.96-32.61 80.57-32.61 32.61-80.57 32.61H197.83Zm516.15-113.18h48.19v-48.19l-48.19 48.19Zm-490.48 0h54.48l120-120h108.69l-120 120h54.72l120-120h108.94l-120 120h54.71l120-120h37.13v-444.34H197.83v481.32l36.74-36.98H343.5l-120 120ZM427-502l-84.24 83q-15 15-36.51 15.38-21.52.38-37.01-15.62-15.24-15-15.24-36.88Q254-478 269.24-493l118.13-118.13q16.86-17.2 39.58-17.2t39.68 17.2L507-571l110.24-110q15-15 36.63-15.38 21.64-.38 37.13 15.62 15 15 15 36.76 0 21.76-15 36.76L546.63-462.63q-17.13 16.96-40.22 16.96-23.08 0-40.04-16.96L427-502ZM197.83-197.83v-564.34 564.34Z"
                      />
                    </svg>
                  </span>
                  <span>پیشنهادهای شگفت انگیز</span>
                  <span
                    class="bg-white w-0 lg:group-hover/under:w-[130px] xl:group-hover/under:w-[155px] 2xl:group-hover/under:w-[160px] rounded-full h-[3px] transition-all ease-linear block absolute bottom-1"
                  ></span>
                </div>
              </nuxt-link>
              <nuxt-link to="/">
                <div
                  class="group/under flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
                >
                  <span>
                    <svg
                      class="xl:w-[24px] xl:h-[24px] lg:w-[16px] lg:h-[16px]"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 48 48"
                    >
                      <ellipse
                        cx="33.164"
                        cy="22.616"
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        rx="8.879"
                        ry="17.083"
                        transform="rotate(-21.248 33.164 22.616)"
                      />
                      <path
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="m37.026 38.831l-26.928-1.447A5.6 5.6 0 0 1 4.5 31.786c0-1.544.772-3.089 1.737-4.15L25.444 7.657"
                      />
                      <path
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M19.46 37.866c-1.93-.193-4.536-3.185-6.177-7.431c-1.64-4.15-1.737-8.011-.58-9.555m26.349 0l-9.555 8.3c2.8 4.922 6.37 7.818 8.88 6.853c3.088-1.255 3.378-8.011.675-15.153m-1.64-3.764l-9.652 8.396a7 7 0 0 1-.29-.772c-2.895-7.431-2.605-14.38.483-15.635c2.703-.965 6.563 2.51 9.459 8.01ZM19.942 38.06c0 2.026-1.64 3.57-3.764 3.57s-3.764-1.544-3.764-3.474v-.483"
                      />
                    </svg>
                  </span>
                  <span>اخبار و مقلات روز</span>
                  <span
                    class="bg-white w-0 lg:group-hover/under:w-[100px] xl:group-hover/under:w-[120px] 2xl:group-hover/under:w-[125px] rounded-full h-[3px] transition-all ease-linear block absolute bottom-1"
                  ></span>
                </div>
              </nuxt-link>
              <nuxt-link to="/">
                <div
                  class="group/under flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
                >
                  <span>
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="xl:w-[24px] xl:h-[24px] lg:w-[16px] lg:h-[16px]"
                      viewBox="0 0 24 24"
                    >
                      <path
                        fill="currentColor"
                        d="M20.6 5.26a2.51 2.51 0 0 0-2.48-2.2H5.885a2.51 2.51 0 0 0-2.48 2.19l-.3 2.47a3.4 3.4 0 0 0 1.16 2.56v8.16a2.5 2.5 0 0 0 2.5 2.5h10.47a2.5 2.5 0 0 0 2.5-2.5v-8.16A3.4 3.4 0 0 0 20.9 7.72Zm-6.59 14.68h-4v-4.08a1.5 1.5 0 0 1 1.5-1.5h1a1.5 1.5 0 0 1 1.5 1.5Zm4.73-1.5a1.5 1.5 0 0 1-1.5 1.5h-2.23v-4.08a2.5 2.5 0 0 0-2.5-2.5h-1a2.5 2.5 0 0 0-2.5 2.5v4.08H6.765a1.5 1.5 0 0 1-1.5-1.5v-7.57a3.2 3.2 0 0 0 1.24.24a3.36 3.36 0 0 0 2.58-1.19a.24.24 0 0 1 .34 0a3.36 3.36 0 0 0 2.58 1.19A3.4 3.4 0 0 0 14.6 9.92a.22.22 0 0 1 .16-.07a.24.24 0 0 1 .17.07a3.36 3.36 0 0 0 2.58 1.19a3.2 3.2 0 0 0 1.23-.24Zm-1.23-8.33a2.39 2.39 0 0 1-1.82-.83a1.2 1.2 0 0 0-.92-.43h-.01a1.2 1.2 0 0 0-.92.42a2.476 2.476 0 0 1-3.65 0a1.24 1.24 0 0 0-1.86 0A2.405 2.405 0 0 1 4.1 7.78l.3-2.4a1.52 1.52 0 0 1 1.49-1.32h12.23a1.5 1.5 0 0 1 1.49 1.32l.29 2.36a2.39 2.39 0 0 1-2.395 2.37Z"
                      />
                    </svg>
                  </span>
                  <span>همکار و قیمت عمده</span>
                  <span
                    class="bg-white w-0 lg:group-hover/under:w-[112px] xl:group-hover/under:w-[140px] 2xl:group-hover/under:w-[145px] rounded-full h-[3px] transition-all ease-linear block absolute bottom-1"
                  ></span>
                </div>
              </nuxt-link>
            </div>
          </div>
          <div class="flex items-center">
            <div class="relative rounded-md shadow-sm">
              <div
                class="pointer-events-none absolute inset-y-0 right-0 flex items-center xl:pr-3 lg:pr-1.5"
              >
                <span class="text-white xl:ml-[10px] lg:pl-1.5">
                  <svg
                    class="2xl:w-[22px] 2xl:h-[22px] xl:w-[16px] xl:h-[16px] lg:w-[14px] lg:h-[14px]"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 -960 960 960"
                    fill="#fff"
                  >
                    <path
                      d="M375.57-295.85q-119.65 0-202.79-83.14-83.13-83.15-83.13-202.82 0-119.67 83.15-202.77 83.14-83.09 202.81-83.09t202.77 83.13q83.1 83.13 83.1 202.78 0 45.48-12.26 85.76-12.26 40.28-35.31 71.57l217.05 217.28q15.95 16.19 15.95 39.5t-16.19 39.52q-16.15 15.96-39.49 15.96-23.34 0-39.53-15.96L536-344.17q-29.87 22.04-72.53 35.18-42.67 13.14-87.9 13.14Zm-.1-113.17q72.99 0 122.91-49.83 49.92-49.82 49.92-122.81 0-72.99-49.92-122.92-49.92-49.92-122.91-49.92t-122.82 49.92q-49.82 49.93-49.82 122.92 0 72.99 49.82 122.81 49.83 49.83 122.82 49.83Z"
                    />
                  </svg>
                </span>
                <span class="bg-white w-[1px] 2xl:h-[28px] lg:h-[20px]"></span>
              </div>
            </div>
            <input
              type="text"
              placeholder="جستوجو در مبیت"
              class="outline-none hidden lg:block placeholder:text-white xl:placeholder:text-xs lg:placeholder:text-[9px] bg-[#fff0] bg-gradient-to-l from-white/15 3xl:w-[700px] 2xl:w-[370px] xl:w-[310px] lg:w-[200px] w-[90%] 2xl:h-[42px] xl:h-[33px] lg:h-[24px] focus:ring-2 ring-white xl:rounded-[12px] lg:rounded-[6px] pl-10 xl:pr-16 2xl:pr-[75px] lg:pr-10 shadow-sm"
            />
          </div>
        </div>
        <div class="hidden lg:flex items-center 2xl:gap-x-10 lg:gap-x-4 mx-5">
          <div>
            <NuxtLink
              to="/"
              class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
            >
              <span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                  viewBox="0 0 24 24"
                >
                  <circle cx="12" cy="6" r="4" fill="currentColor" />
                  <path
                    fill="currentColor"
                    d="M20 17.5c0 2.485 0 4.5-8 4.5s-8-2.015-8-4.5S7.582 13 12 13s8 2.015 8 4.5"
                  />
                </svg>
              </span>
              <span>ورود / ثبت نام</span>
            </NuxtLink>
          </div>
          <div>
            <NuxtLink
              to="/"
              class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
            >
              <span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                  viewBox="0 0 24 24"
                >
                  <g fill="none">
                    <path
                      d="m12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z"
                    />
                    <path
                      fill="currentColor"
                      d="M18.06 3a2 2 0 0 1 1.98 1.719l.017.156l.875 14a2 2 0 0 1-1.847 2.12l-.15.005H5.066a2 2 0 0 1-2-1.976l.003-.149l.875-14a2 2 0 0 1 1.84-1.869L5.94 3zM15 7a1 1 0 0 0-.993.883L14 8a2 2 0 1 1-4 0a1 1 0 0 0-2 0a4 4 0 0 0 8 0a1 1 0 0 0-1-1"
                    />
                  </g>
                </svg>
              </span>
              <span>سبدخرید</span>
            </NuxtLink>
          </div>
        </div>
      </div>
    </header>
    <!-- h1 -->
    <header
      class="hidden invisible lg:block bg-[#1C39BB] px-1.5 w-full text-white shadow-md xl:text-[12.8px] lg:text-[11px]"
    >
      <div class="flex lg:justify-between items-center">
        <div class="items-center lg:mx-0 hidden lg:flex">
          <NuxtLink to="/">
            <div class="2xl:ml-10 xl:ml-7 lg:ml-5 flex items-center">
              <img
                src="~/assets/images/LogoType.png"
                class="2xl:w-[94px] xl:w-[70px] lg:w-[50px] w-20"
                alt="Logo"
              />
            </div>
          </NuxtLink>
          <div class="hidden lg:block">
            <ul
              class="flex items-center 2xl:gap-x-8 xl:gap-x-5 lg:gap-x-4 xl:ml-16 lg:ml-8"
            >
              <li
                class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1 cursor-pointer py-6"
              >
                <span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                    viewBox="0 0 24 24"
                  >
                    <path
                      fill="currentColor"
                      d="M14.116 20q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0-8.5q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14T14.115 4h4.27q.666 0 1.14.475T20 5.615v4.27q0 .666-.475 1.14t-1.14.475zm-8.5 0q-.667 0-1.141-.475T4 9.885v-4.27q0-.666.475-1.14T5.615 4h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0 8.5q-.667 0-1.141-.475T4 18.386v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14T9.885 20z"
                    />
                  </svg>
                </span>
                <span>دسته بندی ها</span>
              </li>
              <nuxt-link to="/shop">
                <li class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1">
                  <span>
                    <svg
                      class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 -960 960 960"
                      fill="#e8eaed"
                    >
                      <path
                        d="M197.83-84.65q-47.96 0-80.57-32.61-32.61-32.61-32.61-80.57v-564.34q0-47.96 32.61-80.57 32.61-32.61 80.57-32.61h564.34q47.96 0 80.57 32.61 32.61 32.61 32.61 80.57v564.34q0 47.96-32.61 80.57-32.61 32.61-80.57 32.61H197.83Zm516.15-113.18h48.19v-48.19l-48.19 48.19Zm-490.48 0h54.48l120-120h108.69l-120 120h54.72l120-120h108.94l-120 120h54.71l120-120h37.13v-444.34H197.83v481.32l36.74-36.98H343.5l-120 120ZM427-502l-84.24 83q-15 15-36.51 15.38-21.52.38-37.01-15.62-15.24-15-15.24-36.88Q254-478 269.24-493l118.13-118.13q16.86-17.2 39.58-17.2t39.68 17.2L507-571l110.24-110q15-15 36.63-15.38 21.64-.38 37.13 15.62 15 15 15 36.76 0 21.76-15 36.76L546.63-462.63q-17.13 16.96-40.22 16.96-23.08 0-40.04-16.96L427-502ZM197.83-197.83v-564.34 564.34Z"
                      />
                    </svg>
                  </span>
                  <span>پیشنهادهای شگفت انگیز</span>
                </li>
              </nuxt-link>
              <nuxt-link to="/">
                <li class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1">
                  <span>
                    <svg
                      class="xl:w-[24px] xl:h-[24px] lg:w-[16px] lg:h-[16px]"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 48 48"
                    >
                      <ellipse
                        cx="33.164"
                        cy="22.616"
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        rx="8.879"
                        ry="17.083"
                        transform="rotate(-21.248 33.164 22.616)"
                      />
                      <path
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="m37.026 38.831l-26.928-1.447A5.6 5.6 0 0 1 4.5 31.786c0-1.544.772-3.089 1.737-4.15L25.444 7.657"
                      />
                      <path
                        fill="none"
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M19.46 37.866c-1.93-.193-4.536-3.185-6.177-7.431c-1.64-4.15-1.737-8.011-.58-9.555m26.349 0l-9.555 8.3c2.8 4.922 6.37 7.818 8.88 6.853c3.088-1.255 3.378-8.011.675-15.153m-1.64-3.764l-9.652 8.396a7 7 0 0 1-.29-.772c-2.895-7.431-2.605-14.38.483-15.635c2.703-.965 6.563 2.51 9.459 8.01ZM19.942 38.06c0 2.026-1.64 3.57-3.764 3.57s-3.764-1.544-3.764-3.474v-.483"
                      />
                    </svg>
                  </span>
                  <span>اخبار و مقلات روز</span>
                </li>
              </nuxt-link>
              <nuxt-link to="/">
                <li class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1">
                  <span>
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      class="xl:w-[24px] xl:h-[24px] lg:w-[16px] lg:h-[16px]"
                      viewBox="0 0 24 24"
                    >
                      <path
                        fill="currentColor"
                        d="M20.6 5.26a2.51 2.51 0 0 0-2.48-2.2H5.885a2.51 2.51 0 0 0-2.48 2.19l-.3 2.47a3.4 3.4 0 0 0 1.16 2.56v8.16a2.5 2.5 0 0 0 2.5 2.5h10.47a2.5 2.5 0 0 0 2.5-2.5v-8.16A3.4 3.4 0 0 0 20.9 7.72Zm-6.59 14.68h-4v-4.08a1.5 1.5 0 0 1 1.5-1.5h1a1.5 1.5 0 0 1 1.5 1.5Zm4.73-1.5a1.5 1.5 0 0 1-1.5 1.5h-2.23v-4.08a2.5 2.5 0 0 0-2.5-2.5h-1a2.5 2.5 0 0 0-2.5 2.5v4.08H6.765a1.5 1.5 0 0 1-1.5-1.5v-7.57a3.2 3.2 0 0 0 1.24.24a3.36 3.36 0 0 0 2.58-1.19a.24.24 0 0 1 .34 0a3.36 3.36 0 0 0 2.58 1.19A3.4 3.4 0 0 0 14.6 9.92a.22.22 0 0 1 .16-.07a.24.24 0 0 1 .17.07a3.36 3.36 0 0 0 2.58 1.19a3.2 3.2 0 0 0 1.23-.24Zm-1.23-8.33a2.39 2.39 0 0 1-1.82-.83a1.2 1.2 0 0 0-.92-.43h-.01a1.2 1.2 0 0 0-.92.42a2.476 2.476 0 0 1-3.65 0a1.24 1.24 0 0 0-1.86 0A2.405 2.405 0 0 1 4.1 7.78l.3-2.4a1.52 1.52 0 0 1 1.49-1.32h12.23a1.5 1.5 0 0 1 1.49 1.32l.29 2.36a2.39 2.39 0 0 1-2.395 2.37Z"
                      />
                    </svg>
                  </span>
                  <span>همکار و قیمت عمده</span>
                </li>
              </nuxt-link>
            </ul>
          </div>
          <div class="flex items-center">
            <div class="relative rounded-md shadow-sm">
              <div
                class="pointer-events-none absolute inset-y-0 right-0 flex items-center xl:pr-3 lg:pr-1.5"
              >
                <span class="text-white xl:ml-[10px] lg:pl-1.5">
                  <svg
                    class="2xl:w-[22px] 2xl:h-[22px] xl:w-[16px] xl:h-[16px] lg:w-[14px] lg:h-[14px]"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 -960 960 960"
                    fill="#fff"
                  >
                    <path
                      d="M375.57-295.85q-119.65 0-202.79-83.14-83.13-83.15-83.13-202.82 0-119.67 83.15-202.77 83.14-83.09 202.81-83.09t202.77 83.13q83.1 83.13 83.1 202.78 0 45.48-12.26 85.76-12.26 40.28-35.31 71.57l217.05 217.28q15.95 16.19 15.95 39.5t-16.19 39.52q-16.15 15.96-39.49 15.96-23.34 0-39.53-15.96L536-344.17q-29.87 22.04-72.53 35.18-42.67 13.14-87.9 13.14Zm-.1-113.17q72.99 0 122.91-49.83 49.92-49.82 49.92-122.81 0-72.99-49.92-122.92-49.92-49.92-122.91-49.92t-122.82 49.92q-49.82 49.93-49.82 122.92 0 72.99 49.82 122.81 49.83 49.83 122.82 49.83Z"
                    />
                  </svg>
                </span>
                <span class="bg-white w-[1px] 2xl:h-[28px] lg:h-[20px]"></span>
              </div>
            </div>
            <input
              type="text"
              placeholder="جستوجو در مبیت"
              class="outline-none hidden lg:block placeholder:text-white xl:placeholder:text-xs lg:placeholder:text-[9px] bg-[#fff0] bg-gradient-to-l from-white/15 3xl:w-[700px] 2xl:w-[370px] xl:w-[310px] lg:w-[200px] w-[90%] 2xl:h-[42px] xl:h-[33px] lg:h-[24px] focus:ring-2 ring-white xl:rounded-[12px] lg:rounded-[6px] pl-10 xl:pr-16 lg:pr-10 shadow-sm"
            />
          </div>
        </div>
        <div class="hidden lg:flex items-center 2xl:gap-x-10 lg:gap-x-4 mx-5">
          <div>
            <NuxtLink
              to="/"
              class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
            >
              <span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                  viewBox="0 0 24 24"
                >
                  <circle cx="12" cy="6" r="4" fill="currentColor" />
                  <path
                    fill="currentColor"
                    d="M20 17.5c0 2.485 0 4.5-8 4.5s-8-2.015-8-4.5S7.582 13 12 13s8 2.015 8 4.5"
                  />
                </svg>
              </span>
              <span>ورود / ثبت نام</span>
            </NuxtLink>
          </div>
          <div>
            <NuxtLink
              to="/"
              class="flex items-center 2xl:gap-x-3 xl:gap-x-2 lg:gap-x-1"
            >
              <span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="xl:w-[20px] xl:h-[20px] lg:w-[14px] lg:h-[14px]"
                  viewBox="0 0 24 24"
                >
                  <g fill="none">
                    <path
                      d="m12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z"
                    />
                    <path
                      fill="currentColor"
                      d="M18.06 3a2 2 0 0 1 1.98 1.719l.017.156l.875 14a2 2 0 0 1-1.847 2.12l-.15.005H5.066a2 2 0 0 1-2-1.976l.003-.149l.875-14a2 2 0 0 1 1.84-1.869L5.94 3zM15 7a1 1 0 0 0-.993.883L14 8a2 2 0 1 1-4 0a1 1 0 0 0-2 0a4 4 0 0 0 8 0a1 1 0 0 0-1-1"
                    />
                  </g>
                </svg>
              </span>
              <span>سبدخرید</span>
            </NuxtLink>
          </div>
        </div>
      </div>
    </header>
    <!-- Header Mobile -->
    <header
      class="lg:hidden inline-block fixed bg-[#1C39BB] w-full sm:px-5 px-3"
    >
      <div class="flex items-center justify-between mt-4">
        <div>
          <svg
            class="text-white"
            xmlns="http://www.w3.org/2000/svg"
            width="26px"
            height="26px"
            viewBox="0 0 32 32"
            fill="currentColor"
          >
            <circle cx="16" cy="8" r="2" fill="currentColor" />
            <circle cx="16" cy="16" r="2" fill="currentColor" />
            <circle cx="16" cy="24" r="2" fill="currentColor" />
          </svg>
        </div>
        <!-- Logo -->
        <NuxtLink to="/">
          <div>
            <img
              src="~/assets/images/LogoType.png"
              class="w-[70px]"
              alt="Logo"
            />
          </div>
        </NuxtLink>
        <div></div>
      </div>
      <!-- Search Box -->
      <div>
        <div class="relative rounded-md shadow-sm">
          <div
            class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-4"
          >
            <span>
              <svg
                class="w-[20px] h-[20px] sm:w-[24px] sm:h-[24px]"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 -960 960 960"
                fill="#fff"
              >
                <path
                  d="M375.57-295.85q-119.65 0-202.79-83.14-83.13-83.15-83.13-202.82 0-119.67 83.15-202.77 83.14-83.09 202.81-83.09t202.77 83.13q83.1 83.13 83.1 202.78 0 45.48-12.26 85.76-12.26 40.28-35.31 71.57l217.05 217.28q15.95 16.19 15.95 39.5t-16.19 39.52q-16.15 15.96-39.49 15.96-23.34 0-39.53-15.96L536-344.17q-29.87 22.04-72.53 35.18-42.67 13.14-87.9 13.14Zm-.1-113.17q72.99 0 122.91-49.83 49.92-49.82 49.92-122.81 0-72.99-49.92-122.92-49.92-49.92-122.91-49.92t-122.82 49.92q-49.82 49.93-49.82 122.92 0 72.99 49.82 122.81 49.83 49.83 122.82 49.83Z"
                />
              </svg>
            </span>
          </div>
          <input
            type="text"
            placeholder="جستوجو در مبیت"
            class="outline-none mx-auto text-white sm:my-5 my-3 lg:hidden block w-full sm:h-[50px] h-[45px] placeholder:text-[#d4d4d4] sm:placeholder:text-xs placeholder:text-[10px] bg-[#fff0] bg-gradient-to-l from-white/15 focus:ring-2 ring-blue-700 sm:rounded-[18px] rounded-[16px] pl-10 sm:pr-14 pr-12 shadow-sm"
          />
        </div>
      </div>
    </header>
    <!-- h2 -->
    <header
      class="lg:hidden inline-block invisible bg-[#1C39BB] w-full sm:px-5 px-3"
    >
      <div class="flex items-center justify-between mt-4">
        <div>
          <svg
            class="text-white"
            xmlns="http://www.w3.org/2000/svg"
            width="26px"
            height="26px"
            viewBox="0 0 32 32"
            fill="currentColor"
          >
            <circle cx="16" cy="8" r="2" fill="currentColor" />
            <circle cx="16" cy="16" r="2" fill="currentColor" />
            <circle cx="16" cy="24" r="2" fill="currentColor" />
          </svg>
        </div>
        <!-- Logo -->
        <NuxtLink to="/">
          <div>
            <img
              src="~/assets/images/LogoType.png"
              class="w-[70px]"
              alt="Logo"
            />
          </div>
        </NuxtLink>
        <div></div>
      </div>
      <!-- Search Box -->
      <div>
        <div class="relative rounded-md shadow-sm">
          <div
            class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-4"
          >
            <span>
              <svg
                class="w-[20px] h-[20px] sm:w-[24px] sm:h-[24px]"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 -960 960 960"
                fill="#fff"
              >
                <path
                  d="M375.57-295.85q-119.65 0-202.79-83.14-83.13-83.15-83.13-202.82 0-119.67 83.15-202.77 83.14-83.09 202.81-83.09t202.77 83.13q83.1 83.13 83.1 202.78 0 45.48-12.26 85.76-12.26 40.28-35.31 71.57l217.05 217.28q15.95 16.19 15.95 39.5t-16.19 39.52q-16.15 15.96-39.49 15.96-23.34 0-39.53-15.96L536-344.17q-29.87 22.04-72.53 35.18-42.67 13.14-87.9 13.14Zm-.1-113.17q72.99 0 122.91-49.83 49.92-49.82 49.92-122.81 0-72.99-49.92-122.92-49.92-49.92-122.91-49.92t-122.82 49.92q-49.82 49.93-49.82 122.92 0 72.99 49.82 122.81 49.83 49.83 122.82 49.83Z"
                />
              </svg>
            </span>
          </div>
          <input
            type="text"
            placeholder="جستوجو در مبیت"
            class="outline-none mx-auto text-white sm:my-5 my-3 lg:hidden block w-full sm:h-[50px] h-[45px] placeholder:text-[#d4d4d4] sm:placeholder:text-xs placeholder:text-[10px] bg-[#fff0] bg-gradient-to-l from-white/15 focus:ring-2 ring-blue-700 sm:rounded-[18px] rounded-[16px] pl-10 sm:pr-14 pr-12 shadow-sm"
          />
        </div>
      </div>
    </header>
    <!-- Header buttom -->
    <div
      class="lg:hidden flex justify-between items-center bg-gray-50 text-zinc-400/80 absolute bottom-0 w-full px-10 py-2 sm:px-20 sm:py-3 shadow-2xl text-[10px] sm:text-xs"
    >
      <div>
        <NuxtLink
          to="/"
          class="flex flex-col items-center justify-center gap-y-1"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="w-[20px] sm:w-[26px]"
            viewBox="0 0 24 24"
          >
            <path
              fill="currentColor"
              d="M13.45 2.533a2.25 2.25 0 0 0-2.9 0L3.8 8.228a2.25 2.25 0 0 0-.8 1.72v9.305c0 .966.784 1.75 1.75 1.75h3a1.75 1.75 0 0 0 1.75-1.75V15.25c0-.68.542-1.232 1.217-1.25h2.566a1.25 1.25 0 0 1 1.217 1.25v4.003c0 .966.784 1.75 1.75 1.75h3a1.75 1.75 0 0 0 1.75-1.75V9.947a2.25 2.25 0 0 0-.8-1.72z"
            />
          </svg>
          <span class="text-zinc-500">صفحه اصلی</span>
        </NuxtLink>
      </div>
      <div>
        <NuxtLink
          to="/"
          class="flex flex-col items-center justify-center gap-y-1"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            class="w-[20px] sm:w-[26px]"
          >
            <path
              fill="currentColor"
              d="M14.116 20q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0-8.5q-.667 0-1.141-.475t-.475-1.14v-4.27q0-.666.475-1.14T14.115 4h4.27q.666 0 1.14.475T20 5.615v4.27q0 .666-.475 1.14t-1.14.475zm-8.5 0q-.667 0-1.141-.475T4 9.885v-4.27q0-.666.475-1.14T5.615 4h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14t-1.14.475zm0 8.5q-.667 0-1.141-.475T4 18.386v-4.27q0-.666.475-1.14t1.14-.475h4.27q.666 0 1.14.475t.475 1.14v4.27q0 .666-.475 1.14T9.885 20z"
            />
          </svg>
          <span class="text-zinc-500">دسته بندی ها</span>
        </NuxtLink>
      </div>
      <div>
        <NuxtLink
          to="/"
          class="flex flex-col items-center justify-center gap-y-1"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="w-[20px] sm:w-[26px]"
            viewBox="0 0 24 24"
          >
            <g fill="none">
              <path
                d="m12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z"
              />
              <path
                fill="currentColor"
                d="M18.06 3a2 2 0 0 1 1.98 1.719l.017.156l.875 14a2 2 0 0 1-1.847 2.12l-.15.005H5.066a2 2 0 0 1-2-1.976l.003-.149l.875-14a2 2 0 0 1 1.84-1.869L5.94 3zM15 7a1 1 0 0 0-.993.883L14 8a2 2 0 1 1-4 0a1 1 0 0 0-2 0a4 4 0 0 0 8 0a1 1 0 0 0-1-1"
              />
            </g>
          </svg>
          <span class="text-zinc-500">سبدخرید</span>
        </NuxtLink>
      </div>
      <div>
        <NuxtLink
          to="/"
          class="flex flex-col items-center justify-center gap-y-1"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="w-[20px] sm:w-[26px]"
            viewBox="0 0 24 24"
          >
            <circle cx="12" cy="6" r="4" fill="currentColor" />
            <path
              fill="currentColor"
              d="M20 17.5c0 2.485 0 4.5-8 4.5s-8-2.015-8-4.5S7.582 13 12 13s8 2.015 8 4.5"
            />
          </svg>
          <span class="text-zinc-500">ورود</span>
        </NuxtLink>
      </div>
    </div>
  </div>
  <div class="border-r-[5px] border-blue-500 rounded-r-[4px]"></div>
</template>

<style scoped>
.borderR {
  border-right-width: 5px;
  border-color: rgb(59 130 246);
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
  padding-right: 12px;
  padding-top: 4px;
  font-size: 13px;
}
</style>
  
<script>
export default {
  data() {
    return {
      dataMegaMenu: {
        dataMobile_1: [
          {
            title: "موبایل و تبلت",
            link: "isLinkMobile",
            img: "mobile.svg",
            child: [
              { title: "گوشی موبایل", link: "mobileLink", BIF: true },
              { title: "شیائومی", link: "#" },
              { title: "سامسونگ", link: "#" },
              { title: "اپل", link: "#" },
              { title: "هواوی", link: "#" },
              { title: "نوکیا", link: "#" },
              { title: "آنر", link: "#" },
              { title: "گوشی های ساده", link: "#" },
              { title: "گلس گوشی موبایل (محافظ صفحه نمایش)", link: "#" },
              { title: "کیف و کاور گوشی", link: "#" },
              { title: "کابل و مبدل", link: "#" },
              { title: "کارت حافظه گوشی موبایل", link: "#" },
              { title: "پایه نگه دارنده تبلت و گوشی", link: "#" },
              { title: "شارژر گوشی", link: "#" },
              { title: "هدفون,هدست,هندزفری", link: "#", BIF: true },
              { title: "باتری گوشی", link: "#" },
              { title: "پاور بانک (شارژر همراه)", link: "#", BIF: true },
              { title: "محافظ لنز دوربین گوشی موبایل", link: "#" },
              { title: "لوازم جانبی موبایل", link: "#", BIF: true },
              { title: "قلم هوشمند", link: "#" },
              { title: "کیف و کاور هندزفری", link: "#" },
              { title: "تبلت", link: "#", BIF: true },
            ],
          },
        ],
        dataJanebi_2: [
          {
            title: "لوازم جانبی موبایل",
            link: "isLinkMobile",
            img: "janebi.webp",
            child: [
              { title: "برند گوشی", link: "mobileLink", BIF: true },
              { title: "لوازم جانبی اپل", link: "#" },
              { title: "لوازم جانبی سامسونگ", link: "#" },
              { title: "لوازم جانبی شیائومی", link: "#" },
              { title: "لوازم جانبی هواوی و آنر", link: "#" },
              { title: "لوازم جانبی نوکیا", link: "#" },
              { title: "لوازم جانبی جی پلاس", link: "#" },
              { title: "لوازم جانبی متورولا", link: "#" },
              { title: "دسته بندی محصولات", link: "#", BIF: true },
              { title: "شارژر", link: "#" },
              { title: "کابل و مبدل", link: "#" },
              { title: "پاور بانک", link: "#" },
              { title: "باتری گوشی موبایل", link: "#" },
              { title: "کارت حافظه گوشی موبایل", link: "#" },
              { title: "کاور و کیف گوشی موبایل", link: "#" },
              { title: "محافظ لنز گوشی موبایل", link: "#" },
              { title: "پایه نگهدارنده گوشی موبایل", link: "#" },
              { title: "گلس و محافظ صفحه گوشی موبایل", link: "#" },
              { title: "هدفون و هندزفری", link: "#" },
              { title: "کیف و کاور هندزفری", link: "#" },
              { title: "اسپیکر بلوتوثی", link: "#" },
              { title: "ساعت هوشمند", link: "#" },
            ],
          },
        ],
        dataLaptop_3: [
          {
            title: "لپ تاپ و کامپیوتر",
            link: "isLinkMobile",
            img: "laptop.svg",
            child: [
              { title: "لپ تاپ", link: "#", BIF: true },
              { title: "کامپیوتر کوچک", link: "#", BIF: true },
              { title: "کامپیوتر All-in-One", link: "#", BIF: true },
              { title: "قطعات اصلی", link: "#", BIF: true },
              { title: "پردازنده", link: "#" },
              { title: "مادربورد", link: "#" },
              { title: "رم کامپیوتر", link: "#" },
              { title: "منبع تغذیه", link: "#" },
              { title: "کارت گرافیک", link: "#" },
              { title: "کیس", link: "#" },
              { title: "هارد دیسک", link: "#" },
              { title: "درایو نوری", link: "#" },
              { title: "فن - خنک کننده", link: "#" },
              { title: "مانیتور", link: "#", BIF: true },
              { title: "اسپیکر", link: "#", BIF: true },
              { title: "جانبی کامپیوتر و لپ تاپ", link: "#", BIF: true },
              { title: "کیبورد", link: "#" },
              { title: "ماوس", link: "#" },
              { title: "مواس پد", link: "#" },
              { title: "کیف هارد", link: "#" },
              { title: "کابل تبدیل و مبدل", link: "#" },
              { title: "کیف و کوله", link: "#" },
              { title: "پایه خنک کننده", link: "#" },
              { title: "براکت هارداینترنال", link: "#" },
              { title: "سایر قطعات جانبی", link: "#" },
              { title: "فلش مموری", link: "#", BIF: true },
              { title: "ذخیره ساز اطلاعات", link: "#", BIF: true },
              { title: "حافظه اکسترنال", link: "#" },
              { title: "حافظه SSD", link: "#" },
              { title: "تجهیزات شبکه", link: "#", BIF: true },
              { title: "دوربین مداربسته", link: "#", BIF: true },
              { title: "نرم افزار", link: "#", BIF: true },
            ],
          },
        ],
        dataGajet_4: [
          {
            title: "گجت های هوشمند",
            link: "isLinkMobile",
            img: "gajet.svg",
            child: [
              { title: "ساعت هوشمند", link: "#", BIF: true },
              { title: "مچ بند هوشمند", link: "#", BIF: true },
              { title: "لوازم جانبی شیایومی", link: "#", BIF: true },
              {
                title: "لوازم جانبی مچ بند و ساعت هوشمند",
                link: "#",
                BIF: true,
              },
            ],
          },
        ],
        dataSoti_5: [
          {
            title: "لوازم صوتی و تصویری",
            link: "isLinkMobile",
            img: "soti.svg",
            child: [
              { title: "تلوزیون", link: "#", BIF: true },
              { title: "سینمای خانگی و ساندبار", link: "#", BIF: true },
              { title: "لوازم جانبی صوتی و تصویری", link: "#", BIF: true },
              { title: "رادیو", link: "#", BIF: true },
            ],
          },
        ],
        dataMashin_6: [
          {
            title: "ماشین های اداری",
            link: "isLinkMobile",
            img: "mashin.svg",
            child: [
              { title: "پرینتر", link: "#", BIF: true },
              { title: "پرینتر لیبل زن و لوازم جانبی", link: "#", BIF: true },
            ],
          },
        ],
        dataConsole_7: [
          {
            title: "کنسول بازی",
            link: "isLinkMobile",
            img: "console.svg",
            child: [
              { title: "کنسول بازی خانگی", link: "#", BIF: true },
              { title: "تجهیزات جانبی کنسول بازی", link: "#", BIF: true },
            ],
          },
        ],
      },
    };
  },
};
</script>