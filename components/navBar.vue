<!--
 * @Date: 2023-01-07 15:35:23
 * @Author: liting luz.liting@gmail.com
 * @LastEditors: liting luz.liting@gmail.com
 * @LastEditTime: 2023-01-09 23:30:12
 * @FilePath: /search/components/NavBar.vue
-->
<script lang="ts" setup>
const colorMode = useColorMode()
</script>

<template>
  <header
    class="search-navbar w-full fixed z-10 drop-shadow-2xl bg-slate-200/50 dark:bg-slate-800/50 backdrop-blur h-16 px-8 flex justify-between items-center"
  >
    <NuxtLink class="text-3xl text-slate-900 dark:text-slate-200 font-bold" to="/">Search</NuxtLink>
    <div class="flex justify-end items-center gap-4">
      <div>
        <div
          v-show="colorMode.preference === 'system'"
          class="i-material-symbols:desktop-windows text-3xl icon-btn"
          @click="colorMode.preference = 'light'"
        ></div>
        <div
          v-show="colorMode.preference === 'light'"
          class="i-material-symbols:light-mode text-3xl icon-btn"
          @click="colorMode.preference = 'dark'"
        ></div>
        <div
          v-show="colorMode.preference === 'dark'"
          class="i-material-symbols:dark-mode text-3xl icon-btn"
          @click="colorMode.preference = 'system'"
        ></div>
      </div>
      <NuxtLink to="https://github.com/liting-yes/search.git" target="__blank">
        <div class="i-mdi:github text-3xl icon-btn"></div>
      </NuxtLink>
    </div>
  </header>
</template>
