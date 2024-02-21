<template>
  <head>
    <title>{{ pageTitle }} | rodrigoacs</title>
  </head>
  <nav>
    <div>
      <RouterLink
        class="link"
        :class="{ active: isActive('/') }"
        to="/"
      >home</RouterLink>
      <RouterLink
        class="link"
        :class="{ active: isActive('/blog') }"
        to="/blog"
      >blog</RouterLink>
      <RouterLink
        class="link"
        :class="{ active: isActive('/cv') }"
        to="/cv"
      >cv</RouterLink>
    </div>
    <div class="theme-language-wrapper">
      <a id="change-language"><img
          width="24"
          height="24"
          src="https://img.icons8.com/fluency/48/usa-circular.png"
          alt="pt-BR language icon"
        /></a>
      <label class="switch">
        <input
          type="checkbox"
          id="change-theme"
          checked=""
        />
        <span class="slider"></span>
      </label>
    </div>
  </nav>
</template>

<script setup>
import { useRoute } from 'vue-router'
import { computed } from 'vue'

const route = useRoute()
const pageTitle = computed(() => getPageTitle(route.path))

function getPageTitle(path) {
  switch (path) {
    case '/':
      return 'home'
    case '/blog':
      return 'blog'
    case '/cv':
      return 'cv'
    default:
      return 'rodrigoacs'
  }
}

function isActive(path) {
  return route.path === path
}

</script>

<style scoped>
.theme-language-wrapper {
  display: flex;
  gap: 10px;
}

.link {
  display: inline-block;
  color: var(--color-text-unfocused);
  text-decoration: none;
  font-size: 1rem;
  font-weight: 400;
  width: 4rem;
  transition: all 0.3s;
}

.link:hover {
  color: var(--color-text-primary);
  font-weight: 500;
}

.link:active {
  transform: scale(0.9);
}

.active {
  color: var(--color-text-primary) !important;
  font-weight: 500 !important;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 4rem 0px;
}

.switch {
  display: block;
  --width-of-switch: 3.5em;
  --height-of-switch: 24px;
  --size-of-icon: 1.4em;
  --slider-offset: 0.3em;
  position: relative;
  width: var(--width-of-switch);
  height: var(--height-of-switch);
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #f0f0f0;
  transition: 0.2s;
  border-radius: 30px;
}

.slider:before {
  position: absolute;
  content: '';
  height: var(--size-of-icon, 1.4em);
  width: var(--size-of-icon, 1.4em);
  border-radius: 20px;
  left: var(--slider-offset, 0.3em);
  top: 50%;
  transform: translateY(-50%);
  background: linear-gradient(40deg, #ff0080, #ff8c00 70%);
  transition: 0.2s;
}

input:checked+.slider {
  background-color: #222222;
}

input:checked+.slider:before {
  left: calc(100% - (var(--size-of-icon, 1.4em) + var(--slider-offset, 0.3em)));
  background: #222222;
  /* change the value of second inset in box-shadow to change the angle and direction of the moon  */
  box-shadow: inset -3px -2px 5px -2px #8983f7, inset -10px -4px 0 0 #a3dafb;
}
</style>
