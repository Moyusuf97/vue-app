<template>
  <div>
    <div class="bg-[#555555]">
      <div
        class="max-w-6xl mx-auto px-4 md:flex hidden justify-between items-center gap-3"
      >
        <div class="flex gap-8 items-center text-white">
          <a href="#" class="py-[14px] hover:underline text-sm font-medium"
            >Företag</a
          >
          <a
            href="#"
            class="py-[14px] hover:underline bg-[#333333] text-[#F2901E] text-sm font-medium px-6"
            >Privatperson</a
          >
        </div>
        <a
          :href="login"
          class="bg-[#F29008] text-white py-1.5 px-2 rounded-md text-sm transition-all hover:bg-[#EF7E0B]"
        >
          Logga in
        </a>
      </div>
    </div>
    <!--  -->
    <nav class="bg-[#333333]">
      <div
        class="max-w-6xl mx-auto py-6 lg:px-0 px-4 flex justify-between items-center gap-2"
      >
        <div class="flex gap-10">
          <img src="./logo.svg" alt="" class="w-24 h-auto" />
          <div class="md:flex hidden items-center lg:gap-10 gap-2">
            <div class="flex group gap-8">
              <div class="flex items-center gap-1">
                <a
                  href="#"
                  class="group-hover:border-b-[2px] peer hover:border-[#008EAA] text-[17px] text-white"
                >
                  Produkter & tjänster
                </a>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-[#97B3C0] group-hover:text-white cursor-pointer"
                  width="20"
                  height="20"
                  viewBox="0 0 20 20"
                >
                  <path fill="currentColor" d="m5 6l5 5l5-5l2 1l-7 7l-7-7z" />
                </svg>
              </div>
              <div
                class="w-[100%] absolute group-hover:flex hidden top-[160px] left-0 bg-[#333333] text-white"
              >
                <div
                  class="grid lg:grid-cols-3 grid-cols-2 gap-3 px-20 py-10 max-w-7xl mx-auto"
                >
                  <div v-for="p in products" :key="p" class="cursor-pointer">
                    <h3 class="font-bold text-xl">{{ p.title }}</h3>
                    <div class="pt-6 flex flex-col gap-6">
                      <div class="">
                        <div
                          v-for="i in p.menuItems"
                          :key="i"
                          class="flex group items-start gap-3"
                        >
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="group-hover:text-[#EF7E0B]"
                            width="22"
                            height="22"
                            viewBox="0 0 14 14"
                          >
                            <path
                              fill="none"
                              stroke="currentColor"
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              d="m1.24 6.54l11.5-5.23M10.59.5l2.15.81l-.8 2.15m1.31 10.04h-2.5v-7a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5zm-5 0h-2.5V8a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5zm-5 0H.75v-4a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5z"
                            />
                          </svg>
                          <div class="">
                            <a
                              href="#"
                              class="group-hover:border-b-[2px] group-hover:border-[#008EAA] text-lg font-medium"
                            >
                              {{ i.title }}
                            </a>
                            <p class="text-[17px] text-[#A5C0C0] pt-1">
                              {{ i.teaserText }}
                            </p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>

                  <!-- <div class="cursor-pointer">
                    <h3 class="font-bold text-xl">Känn dig trygg</h3>
                    <div class="pt-6 flex flex-col gap-6">
                      <div class="">
                        <div class="flex group items-start gap-3">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="mt-1 group-hover:text-[#EF7E0B]"
                            width="20"
                            height="20"
                            viewBox="0 0 48 48"
                          >
                            <g
                              fill="none"
                              stroke="currentColor"
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              stroke-width="4"
                            >
                              <circle cx="24" cy="11" r="7" />
                              <path
                                d="M4 41c0-8.837 8.059-16 18-16m6 4.2c0-1.067 7-3.2 7-3.2s7 2.133 7 3.2c0 8.533-7 12.8-7 12.8s-7-4.267-7-12.8"
                              />
                            </g>
                          </svg>
                          <div class="">
                            <a
                              href="#"
                              class="group-hover:border-b-[2px] group-hover:border-[#008EAA] text-lg font-medium"
                            >
                              ID-Skydd
                            </a>
                            <p class="text-[17px] text-[#A5C0C0] pt-1">
                              Löpande bevakning av dina <br />
                              personliga uppgifter
                            </p>
                          </div>
                        </div>
                      </div>
                      <div class="">
                        <div class="flex group items-start gap-3">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="group-hover:text-[#EF7E0B]"
                            width="22"
                            height="22"
                            viewBox="0 0 24 24"
                          >
                            <path
                              fill="none"
                              stroke="currentColor"
                              stroke-linecap="round"
                              stroke-linejoin="round"
                              stroke-width="2"
                              d="M19.506 7.96A16.027 16.027 0 0 1 7.96 19.506C5.819 20.051 4 18.21 4 16v-1c0-.552.449-.995.999-1.05a9.94 9.94 0 0 0 2.656-.639l1.519 1.52a12.049 12.049 0 0 0 5.657-5.657l-1.52-1.52a9.94 9.94 0 0 0 .64-2.656C14.005 4.448 14.448 4 15 4h1c2.208 0 4.05 1.819 3.505 3.96"
                            />
                          </svg>
                          <div class="">
                            <a
                              href="#"
                              class="group-hover:border-b-[2px] group-hover:border-[#008EAA] text-lg font-medium"
                            >
                              Förlustanmälan
                            </a>
                            <p class="text-[17px] text-[#A5C0C0] pt-1">
                              Anmäl borttappade ID- <br />
                              handlingar
                            </p>
                          </div>
                        </div>
                      </div>
                      <div class="">
                        <div class="flex group items-start gap-3">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="mt-1 group-hover:text-[#EF7E0B]"
                            width="20"
                            height="20"
                            viewBox="0 0 24 24"
                          >
                            <g fill="none">
                              <path
                                d="M24 0v24H0V0zM12.593 23.258l-.011.002l-.071.035l-.02.004l-.014-.004l-.071-.035c-.01-.004-.019-.001-.024.005l-.004.01l-.017.428l.005.02l.01.013l.104.074l.015.004l.012-.004l.104-.074l.012-.016l.004-.017l-.017-.427c-.002-.01-.009-.017-.017-.018m.265-.113l-.013.002l-.185.093l-.01.01l-.003.011l.018.43l.005.012l.008.007l.201.093c.012.004.023 0 .029-.008l.004-.014l-.034-.614c-.003-.012-.01-.02-.02-.022m-.715.002a.023.023 0 0 0-.027.006l-.006.014l-.034.614c0 .012.007.02.017.024l.015-.002l.201-.093l.01-.008l.004-.011l.017-.43l-.003-.012l-.01-.01z"
                              />
                              <path
                                fill="currentColor"
                                d="M11.298 2.195a2 2 0 0 1 1.232-.055l.172.055l7 2.625a2 2 0 0 1 1.291 1.708l.007.165v5.363a9 9 0 0 1-4.709 7.911l-.266.139l-3.354 1.677a1.5 1.5 0 0 1-1.198.062l-.144-.062l-3.354-1.677a9 9 0 0 1-4.97-7.75l-.005-.3V6.693a2 2 0 0 1 1.145-1.808l.153-.065zM12 4.068L5 6.693v5.363a7 7 0 0 0 3.635 6.138l.235.123L12 19.882l3.13-1.565a7 7 0 0 0 3.865-5.997l.005-.264V6.693zm3.433 4.561a1 1 0 0 1 1.497 1.32l-.083.094l-5.234 5.235a1.1 1.1 0 0 1-1.46.085l-.096-.085l-2.404-2.404a1 1 0 0 1 1.32-1.498l.094.083l1.768 1.768z"
                              />
                            </g>
                          </svg>
                          <div class="">
                            <a
                              href="#"
                              class="group-hover:border-b-[2px] group-hover:border-[#008EAA] text-lg font-medium"
                            >
                              Bedrägerispärr
                            </a>
                            <p class="text-[17px] text-[#A5C0C0] pt-1">
                              Spärra din kreditupplysning
                            </p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div> -->
                  <div
                    class="bg-[url('./link1bg.png')] bg-cover h-fit px-6 py-10"
                  >
                    <h1 class="text-2xl font-bold text-white">
                      Vinn ett ID-Skydd
                    </h1>
                    <p class="text-white text-lg pt-2">
                      Undvik ID-kaparen och samla poäng genom att fånga
                      ID-skyddet.
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <div class="flex group gap-4">
              <div class="flex group items-center gap-1">
                <a
                  href="#"
                  class="group-hover:border-b-[2px] hover:border-[#008EAA] text-[17px] text-white"
                >
                  Artiklar & kunskap
                </a>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="text-[#97B3C0] group-hover:text-white cursor-pointer"
                  width="20"
                  height="20"
                  viewBox="0 0 20 20"
                >
                  <path fill="currentColor" d="m5 6l5 5l5-5l2 1l-7 7l-7-7z" />
                </svg>
              </div>

              <div
                class="w-[100%] group-hover:flex hidden absolute top-[160px] left-0 bg-[#333333] text-white"
              >
                <div
                  class="grid lg:grid-cols-3 grid-cols-2 gap-3 px-20 py-10 max-w-7xl mx-auto"
                >
                  <div class="cursor-pointer">
                    <h3 class="font-bold text-xl">{{ category.title }}</h3>
                    <div class="pt-6 flex flex-col gap-6">
                      <div
                        v-for="cat in category.menuItems"
                        :key="cat"
                        class=""
                      >
                        <div class="flex group items-start gap-3">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="group-hover:text-[#EF7E0B]"
                            width="20"
                            height="20"
                            viewBox="0 0 32 32"
                          >
                            <path
                              fill="currentColor"
                              d="M7 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v18H7zm2 22a2 2 0 0 1-2-2h18.25A1.75 1.75 0 0 0 27 24.25V6a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v20a4 4 0 0 0 4 4h17a1 1 0 1 0 0-2zm1.75-22A1.75 1.75 0 0 0 9 7.75v2.5c0 .966.784 1.75 1.75 1.75h10.5A1.75 1.75 0 0 0 23 10.25v-2.5A1.75 1.75 0 0 0 21.25 6zm.25 4V8h10v2z"
                            />
                          </svg>
                          <div class="">
                            <a
                              href="#"
                              class="group-hover:border-b-[2px] group-hover:border-[#008EAA] text-lg font-medium"
                            >
                              {{ cat.title }}
                            </a>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>

                  <div class="cursor-pointer">
                    <h3 class="font-bold text-xl">{{ articles.title }}</h3>

                    <div class="pt-6 flex flex-col gap-3">
                      <div
                        class=""
                        v-for="article in articles.menuItems"
                        :key="article"
                      >
                        <div class="flex group items-start gap-3">
                          <div class="">
                            <a
                              href="#"
                              class="hover:border-b-[2px] hover:border-[#008EAA] text-lg font-medium"
                            >
                              {{ article.title }}
                            </a>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div
                    class="bg-[url('./link2.png')] bg-cover h-fit px-6 py-10"
                  >
                    <h1 class="text-2xl font-bold text-white">
                      Hur tryggt är ditt <br />
                      personnummer?
                    </h1>
                    <p class="text-white text-lg pt-2">
                      Gör vårt test på
                      <a
                        href="#"
                        class="text-[#F29008] hover:underline font-medium"
                      >
                        idsmart.se
                      </a>
                      och se själv.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="sm:flex flex-row hidden">
            <div class="flex md:hidden text-white items-center">
              <a href="#" class="text-sm"
                ><span class="text-[#848484]">Min UC Företag |</span>
                Privatperson</a
              >
            </div>
          </div>
        </div>
        <div class="md:flex hidden group items-center gap-3">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="text-[#C0C0C0] group-hover:text-[#EF7E0B]"
            width="22"
            height="22"
            viewBox="0 0 512 512"
          >
            <path
              fill="currentColor"
              d="M256 8C119.033 8 8 119.033 8 256s111.033 248 248 248s248-111.033 248-248S392.967 8 256 8m173.696 119.559l-63.399 63.399c-10.987-18.559-26.67-34.252-45.255-45.255l63.399-63.399a218.396 218.396 0 0 1 45.255 45.255M256 352c-53.019 0-96-42.981-96-96s42.981-96 96-96s96 42.981 96 96s-42.981 96-96 96M127.559 82.304l63.399 63.399c-18.559 10.987-34.252 26.67-45.255 45.255l-63.399-63.399a218.372 218.372 0 0 1 45.255-45.255M82.304 384.441l63.399-63.399c10.987 18.559 26.67 34.252 45.255 45.255l-63.399 63.399a218.396 218.396 0 0 1-45.255-45.255m302.137 45.255l-63.399-63.399c18.559-10.987 34.252-26.67 45.255-45.255l63.399 63.399a218.403 218.403 0 0 1-45.255 45.255"
            />
          </svg>
          <a
            :href="help"
            class="group-hover:border-b-[2px] hover:border-[#008EAA] text-[17px] text-[#A5C0C0]"
          >
            Hjälp & kontakt
          </a>
        </div>
        <div class="flex md:hidden gap-4 justify-end">
          <div
            class="h-8 flex items-center justify-center cursor-ointer w-8 transition-all hover:bg-[#EF7E0B] bg-[#F29008] text-white rounded"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 16 16"
            >
              <path
                fill="currentColor"
                d="M11 5a3 3 0 1 1-6 0a3 3 0 0 1 6 0M8 7a2 2 0 1 0 0-4a2 2 0 0 0 0 4m0 5.996V14H3s-1 0-1-1s1-4 6-4q.845.002 1.544.107a4.5 4.5 0 0 0-.803.918A11 11 0 0 0 8 10c-2.29 0-3.516.68-4.168 1.332c-.678.678-.83 1.418-.832 1.664zM9 13a1 1 0 0 1 1-1v-1a2 2 0 1 1 4 0v1a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-4a1 1 0 0 1-1-1zm3-3a1 1 0 0 0-1 1v1h2v-1a1 1 0 0 0-1-1"
              />
            </svg>
          </div>
          <div
            class="h-8 flex items-center justify-center cursor-pointer w-16 rounded-full transition-all hover:bg-[#036D8d] bg-[#036D82] text-white"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
            >
              <path
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M5 17h14M5 12h14M5 7h14"
              />
            </svg>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  products: Object,
  articles: Object,
  category: Object,
  login: String,
  help: String,
});
</script>
