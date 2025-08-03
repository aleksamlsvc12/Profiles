<script setup>
  import Profile from '@/components/Profile.vue';
  import profiles from '@/assets/data/profiles.json';
</script>

<template>
  <div class="p-[5%] grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 justify-items-center gap-6 md:gap-10 h-full overflow-y-auto">
    <div v-for="profile in profiles" :key="profile.id">
      <Profile 
        :name = "profile.name"
        :status = "profile.status"
        :email = "profile.email"
        :followers = "profile.followers"
        :following = "profile.following"
        :posts = "profile.posts"
        :hourlyRate = "profile.hourlyRate"
        :about = "profile.about"
        :location = "profile.location"
      />
    </div>
  </div>
</template>



