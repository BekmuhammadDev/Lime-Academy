<script>
</script>

<template>
  <main>
    <div class="p-6">
      <div class="flex justify-between gap-20">
        <div class="bg-gradient-to-b w-full  from-[#8798C5] to-[#8597C4]  p-6 rounded-xl flex justify-between">
          <div>
            <div class="w-[400px]">
              <div class="mb-5">
                <select name="" id="">
                  <option value="">Uz</option>
                  <option value="">Ru</option>
                </select>
              </div>

              <form @submit.prevent="handleSubmit"
                class="bg-white p-6 rounded-2xl shadow px-8 md:px-14 flex flex-col gap-4 max-w-md mx-auto">
                <input type="password" v-model="oldPassword" placeholder="Ваш старый пароль"
                  class="border px-4 py-2 rounded-2xl" required />

                <input type="password" v-model="newPassword" placeholder="Ваш новый пароль"
                  class="border px-4 py-2 rounded-2xl" required />

                <div class="flex justify-center">
                  <button type="submit" class="bg-[#D9D9D980] text-black py-2 px-6 rounded-lg transition">
                    Изменить
                  </button>
                </div>
              </form>

            </div>

            <div class="flex gap-4 mt-10 items-center">
              <a href="https://facebook.com" target="_blank">
                <i class="bi bi-facebook text-white" style="font-size: 24px;"></i>
              </a>
              <a href="https://instagram.com" target="_blank" class="transition">
                <Instagram class="w-7 h-7 text-white" />
              </a>
              <a href="https://tiktok.com" target="_blank" class=" transition">
                <Music2 stroke-width="4" class="w-7 h-7 text-white" />
              </a>
              <a href="https://youtube.com" target="_blank" class=" transition">
                <Youtube class="w-7 h-7 text-white" />
              </a>
              <a href="https://t.me/yourchannel" target="_blank">
                <i class="bi bi-telegram text-white" style="font-size: 24px;"></i>
              </a>
            </div>
          </div>
          <div>
            <div class="flex items-center mb-3 justify-between">
              <h1 class="text-[32px] font-bold text-white">Профиль</h1>
              <div class="relative left-14 cursor-pointer" @click="toggleLike">
                <span><i class="bi bi-heart-fill text-red-500" style="font-size: 24px;"></i></span>
              </div>
            </div>
            <div class="flex items-center gap-4">
              <div>
                <img src="https://picsum.photos/id/1/200/300" class="rounded-full h-14 w-14" alt="">
              </div>
              <div>
                <p class="font-medium text-white">Donyorov Nizomiddin</p>
                <p class="text-sm text-white">example@gmail.com</p>
              </div>
            </div>
            <div class="mt-4 text-sm flex items-center gap-5 space-y-1">
              <div>
                <p class="text-xs font-bold text-white">Подписки:</p>
                <p class="text-center font-bold text-white">5</p>
              </div>
              <div>
                <p class="text-xs font-bold text-white">Наставник: </p>
                <p class="text-center font-bold text-white">asnaa99</p>
              </div>
              <div>
                <p class="text-xs font-bold text-white">Подписчики: </p>
                <p class="text-center font-bold text-white">50</p>
              </div>
            </div>
            <div class="flex justify-center mt-20">
              <button class="mt-4 bg-[#FFFFFFBF] text-black font-bold px-4 py-3 rounded">Добавить друга</button>
            </div>
          </div>
        </div>

        <div class="flex gap-6 w-full ">
          <div class="bg-white p-4 w-full shadow-md  rounded-xl ">
            <p class="text-center mb-3 font-bold text-[#A9A9A9]">Ваш баланс</p>

            <div class="text-3xl font-bold flex justify-center items-center text-gray-800 gap-2"><span
                class="text-sm pt-3">Lime</span>
              <h1>21.533.10</h1>
            </div>

            <div class="flex justify-center mt-5">
              <div class="flex items-center gap-2  px-4 py-2 rounded-full cursor-pointer" @click="toggleDropdown">
                <img src="https://picsum.photos/id/1/200/300" alt="Lime logo"
                  class="w-6 h-6 rounded-full object-cover" />
                <span class="font-medium">Lime/LIME</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 transition-transform duration-200"
                  :class="{ 'rotate-180': open }" fill="none" viewBox="0 0 24 24" stroke="currentColor"
                  stroke-width="2">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
                </svg>
              </div>
            </div>

            <div class="mt-4 flex gap-5 justify-between text-sm">
              <div>
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-[#0000001F] rounded-full flex items-center justify-center p-2">
                    <SignalMedium class="w-5 h-5 justify-center" stroke-width="4" />
                  </div>

                  <h2 class="text-sm font-bold text-black">Earnings</h2>
                </div>

                <div class="flex gap-2 mb-3">
                  <h5 class="mt-1 font-bold text-xl">7.048</h5>
                  <h1 class="text-2xl font-bold text-black">
                    Lime
                  </h1>
                </div>
                <div class="">
                  <img :src="blackChart" alt="Black Chart" />
                </div>
              </div>

              <div>
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-[#F9A1351F] rounded-full flex items-center justify-center p-2">
                    <SignalMedium color="#F9A135" class="w-5 h-5 justify-center" stroke-width="4" />
                  </div>
                  <h2 class="text-sm font-bold text-black">Earnings</h2>
                </div>

                <div class="flex gap-2 mb-3">
                  <h5 class="mt-1 font-bold text-xl text-[#f9a135]">7.048</h5>
                  <h1 class="text-2xl text-[#f9a135] font-bold">
                    Lime
                  </h1>
                </div>
                <div class="">
                  <img :src="brownChart" alt="Brown Chart" />
                </div>
              </div>

            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>