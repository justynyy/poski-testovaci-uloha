<script setup>
import Navbar from "./components/Navbar.vue"
import Socials from "./components/Socials.vue"
import SideMenu from "./components/SideMenu.vue"
import Footer from "./components/Footer.vue"
</script>

<template>
  <div>
    <Navbar />
    <Socials />
    <SideMenu />
    <router-view v-slot="{ Component, route }">
      <div :key="route.name">
        <component :is="Component" />
      </div>
    </router-view>
    <Footer />
  </div>
</template>

<script>
setTimeout(() => {
  const count = document.querySelectorAll(".article-title").length
  console.log("Počet příspěvků: " + count)

  const item = document.querySelector(".grid-item")
  const height = item.offsetHeight
  console.log("Průměrná výška příspěvků: " + height + "px")

  let length = 0
  const titles = document.querySelectorAll(".article-title")
  titles.forEach((el) => {
    length += el.textContent.trim().length
  })

  console.log("Součet délek nadpisů příspěvků: " + length)
}, 1000)
</script>
