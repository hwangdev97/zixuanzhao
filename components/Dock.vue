<script setup lang="ts">
import 'dockbar'

const socialMedias: DockLinkItem[] = [
  {
    route: 'https://www.instagram.com/iamjoshellis/',
    icon: 'i-carbon-logo-instagram',
  },
  {
    route: 'https://www.linkedin.com/in/joshuaellis/',
    icon: 'i-carbon-logo-linkedin',
  },
  {
    route: 'https://www.facebook.com/strikingly',
    icon: 'i-carbon-logo-facebook',
  },
]

const pageItems: DockLinkItem[] = [
  {
    route: '/',
    icon: 'i-carbon-home',
  },
  {
    route: '/about',
    icon: 'i-carbon-person',
  },
  {
    route: '/projects',
    icon: 'i-carbon-portfolio',
  },
  {
    route: '/contact',
    icon: 'i-carbon-notebook',
  },
]
</script>

<template>
  <dock-wrapper id="dock">
    <dock-item v-for="content in pageItems" :key="content.route">
      <DockButton :dock-link-item="content" />
    </dock-item>

    <div class="divide bg-warmGray dark:bg-gray-9" />

    <dock-item v-for="socialMedia in socialMedias" :key="socialMedia.route">
      <DockButton :dock-link-item="socialMedia" />
    </dock-item>
    <div class="divide bg-warmGray dark:bg-gray-9" />

    <dock-item>
      <DarkToggle class="item border bg-white dark:border-black dark:bg-black" />
    </dock-item>
  </dock-wrapper>
</template>

<style scoped>
#dock {
  position: fixed;
  height: 80px;
  display: flex;
  align-items: center;
  left: 50%;
  bottom: 30px;
  transform: translateX(-50%);
  background: linear-gradient(180deg, #76767625 0%, #6c6c6c0e 100%);
  border-radius: 999px;
  border: 1px solid #00000021;
}

.item {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
}

.divide {
  width: 1px;
  height: 100%;
  margin: 0px 6px ;
}
</style>
