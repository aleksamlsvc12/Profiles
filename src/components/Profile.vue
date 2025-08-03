<script setup>
  const props = defineProps({
    name: String,
    status: String,
    email: String,
    followers: Number,
    following: Number,
    posts: Number,
    hourlyRate: Number,
    about: String,
    location: String,
    profilePic: String,
    wallpaper: String
  });
</script>

<template>
  <div class="w-full min-w-[260px] min-h-[500px] md:w-[90%] rounded-3xl shadow-[0_0_10px_1px_rgba(0,0,0,0.4)] overflow-hidden">
    <div class="w-full h-1/3 relative">
      <img :src="wallpaper" alt="cover photo" class="w-full h-full"></img>
      <div class="absolute left-[6%] bottom-[-30%] size-[80px] rounded-full bg-white p-1">
        <img :src="profilePic" alt="profile picture" class="w-full h-full rounded-full">
      </div>
    </div>

    <div class="mt-[20%] pl-[8%] pr-[8%] pb-[5%] flex flex-col">
      <div class="flex items-center">
        <span class="font-bold mr-[3%]">{{ name }}</span>
        <div v-if="status === 'following'" class="text-[10px] border border-gray-300 flex items-center p-[1px] pr-2 pl-2 gap-1 rounded-md">
          <span class="pi pi-circle-fill text-green-600"></span>
          <span class="text-green-600">{{ status }}</span>
        </div>

        <div v-else class="text-[10px] border border-gray-300 flex items-center p-[1px] pr-2 pl-2 gap-1 rounded-md">
          <span class="pi pi-circle-fill text-red-600"></span>
          <span class="text-red-600">{{ status }}</span>
        </div>
      </div>

      <span class="gray text-xs mb-[5%] cursor-pointer">{{ email }}</span>

      <div class="text-xs grid grid-cols-4 mb-[5%]">
        <div class="flex flex-col">
          <span class="gray">Followers</span>
          <span>{{ followers }}</span>
        </div>

        <div class="flex flex-col">
          <span  class="gray">Following</span>
          <span>{{ following }}</span>
        </div>

        <div class="flex flex-col">
          <span class="gray">Posts</span>
          <span>{{ posts }}</span>
        </div>

        <div class="flex flex-col">
          <span class="gray">Hourly Rate</span>
          <span>{{ hourlyRate }}&dollar;</span>
        </div>
      </div>

      <hr class="gray border-dotted mb-[5%]">

      <p class="font-bold text-sm">About</p>
      <p class="text-[10px] text-justify gray mb-[10%]">{{ about }}</p>

      <div class="flex justify-between items-center">
        <div class="flex gap-3">
          <span class="pi pi-github text-sm" ></span>
          <span class="pi pi-linkedin text-sm"></span>
        </div>

        <div class="flex items-center gray gap-1">
          <span class="pi pi-map-marker text-xs"></span>
          <span class="text-[10px] underline cursor-pointer">{{ location }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
  .gray{
    color: rgb(170, 170, 170);
  }

  .pi{
    cursor: pointer;
  }

  .pi-circle-fill{
    cursor: default;
  }
</style>