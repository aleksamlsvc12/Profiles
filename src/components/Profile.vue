<script setup>
  import img from '@/assets/img/img.jpg';
  import profile from '@/assets/img/profile.jpg';
  import profiles from '@/assets/data/profiles.json';
</script>

<template>
  <div class="w-full min-w-[260px] min-h-[500px] md:w-[90%] rounded-3xl shadow-[0_0_10px_1px_rgba(0,0,0,0.4)] overflow-hidden">
    <div class="w-full h-1/3 relative">
      <img :src="img" alt="cover photo" class="w-full h-full"></img>
      <div class="absolute left-[6%] bottom-[-30%] size-[80px] rounded-full bg-white p-1">
        <img :src="profile" alt="profile picture" class="w-full h-full rounded-full">
      </div>
    </div>

    <div class="mt-[20%] pl-[8%] pr-[8%] pb-[5%] flex flex-col">
      <div class="flex items-center">
        <span class="font-bold mr-[3%]">{{ profiles.p1.name }}</span>
        <div class="text-[10px] border border-gray-300 flex items-center p-[1px] pr-2 pl-2 gap-1 rounded-md">
           <span class="pi pi-circle-fill text-green-600"></span>
          <span class="text-green-600">{{ profiles.p1.status }}</span>
        </div>
      </div>

      <span class="gray text-xs mb-[5%] cursor-pointer">{{ profiles.p1.email }}</span>

      <div class="text-xs grid grid-cols-4 mb-[5%]">
        <div class="flex flex-col">
          <span class="gray">Followers</span>
          <span>{{ profiles.p1.followers }}</span>
        </div>

        <div class="flex flex-col">
          <span  class="gray">Following</span>
          <span>{{ profiles.p1.following }}</span>
        </div>

        <div class="flex flex-col">
          <span class="gray">Posts</span>
          <span>{{ profiles.p1.posts }}</span>
        </div>

        <div class="flex flex-col">
          <span class="gray">Hourly Rate</span>
          <span>{{ profiles.p1.hourlyRate }}</span>
        </div>
      </div>

      <hr class="gray border-dotted mb-[5%]">

      <p class="font-bold text-sm">About</p>
      <p class="text-[10px] text-justify gray mb-[10%]">{{ profiles.p1.about }}</p>

      <div class="flex justify-between items-center">
        <div class="flex gap-3">
          <span class="pi pi-github text-sm"></span>
          <span class="pi pi-linkedin text-sm"></span>
          <span class="pi pi-twitter text-sm"></span>
        </div>

        <div class="flex items-center gray gap-1">
          <span class="pi pi-map-marker text-xs"></span>
          <span class="text-[10px] underline cursor-pointer">{{ profiles.p1.location }}</span>
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