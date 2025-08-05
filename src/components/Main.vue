<script setup>
import Profile from "@/components/Profile.vue";

import profiles from "@/assets/data/profiles.json";

import p0 from "@/assets/img/p0.jpg";
import p1 from "@/assets/img/p1.jpg";
import p2 from "@/assets/img/p2.jpg";
import p3 from "@/assets/img/p3.jpg";
import p4 from "@/assets/img/p4.jpg";
import p5 from "@/assets/img/p5.jpg";
import p6 from "@/assets/img/p6.jpg";
import p7 from "@/assets/img/p7.jpg";
import p8 from "@/assets/img/p8.jpg";
import p9 from "@/assets/img/p9.jpg";

import wp0 from "@/assets/img/wp0.jpg";
import wp1 from "@/assets/img/wp1.jpg";
import wp2 from "@/assets/img/wp2.jpg";
import wp3 from "@/assets/img/wp3.jpg";
import wp4 from "@/assets/img/wp4.jpg";
import wp5 from "@/assets/img/wp5.jpg";
import wp6 from "@/assets/img/wp6.jpg";
import wp7 from "@/assets/img/wp7.jpg";
import wp8 from "@/assets/img/wp8.jpg";
import wp9 from "@/assets/img/wp9.jpg";

const profilePics = [p0, p1, p2, p3, p4, p5, p6, p7, p8, p9];
const wallpapers = [wp0, wp1, wp2, wp3, wp4, wp5, wp6, wp7, wp8, wp9];
</script>

<template>
  <div
    class="p-[5%] grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 justify-items-center gap-10 xl:gap-x-30 h-full overflow-y-auto"
  >
    <div v-for="profile in profiles" :key="profile.id">
      <Profile
        :name="profile.name"
        :status="profile.status"
        :email="profile.email"
        :followers="profile.followers"
        :following="profile.following"
        :posts="profile.posts"
        :hourlyRate="profile.hourlyRate"
        :about="profile.about"
        :location="profile.location"
        :profilePic="profilePics[profile.id]"
        :wallpaper="wallpapers[profile.id]"
      />
    </div>
  </div>
</template>

<style>
  body{
    user-select: none;
  }
</style>
