<template>
  <div class="">
    <header class="shadow-lg bg-white min-w-full h-[64px] sticky top-0 z-50">
      <nav class="mx-auto p-3 flex justify-between align-start">
        <NuxtLink to="/" class="font-bold text-2xl text-slate-700"
          >The Dev Guide</NuxtLink
        >
        <ul class="flex gap-4 justify-center align-middle p-3">
          <li><NuxtLink class="btn" to="/">Home</NuxtLink></li>
          <li><NuxtLink class="btn" to="/about">About</NuxtLink></li>
          <li><NuxtLink class="btn" to="/video">Videos</NuxtLink></li>
          <li><NuxtLink class="btn" to="/blog">Blogs</NuxtLink></li>
        </ul>
      </nav>
    </header>

    <!-- output the page -->
    <main class="bg-slate-500 h-[calc(100vh-64px)] overflow-auto">
      <div class="container mx-auto bg-white p-3 min-h-full">
        <slot />
      </div>
    </main>
    <!-- <footer class="py-5 bg-gray-700 text-center min-w-full text-white"></footer> -->
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
li .router-link-exact-active {
  color: green;
}
</style>
