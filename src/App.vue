<script>
import { RouterLink, RouterView } from 'vue-router'

export default {
  components: {
    RouterLink,
    RouterView
  }
}
</script>

<template>
  <header class="nav-header">
    <img alt="Vue logo" class="pulsating-image" src="@/assets/logo.svg" width="60" height="60" />

    <nav>
      <RouterLink to="/" :class="{ active: $route.path === '/' }">📃 notes list</RouterLink>
      <RouterLink
        to="/new"
        :class="{ active: $route.path.includes('/edit') || $route.path.includes('/new') }"
        >➕ add/edit note</RouterLink
      >
    </nav>
  </header>
  <div class="main-container">
    <RouterView />
  </div>
</template>

<style lang="scss" scoped>
@import './App.styles.scss';
</style>
