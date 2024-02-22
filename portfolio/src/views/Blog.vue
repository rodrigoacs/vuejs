<template>
  <div>
    <h2>{{ $t("blog.title") }}</h2>
    <a
      href="#"
      class="blog-post-link"
    >
      <!-- <div class="blog-post">
        <b>Em Breve</b>
        <p>...</p>
      </div> -->
    </a>
  </div>
</template>

<script setup></script>

<style scoped>
.blog-post b {
  color: var(--color-text-secondary);
}

.blog-post {
  margin-top: 1rem;
  padding-bottom: 0.5rem;
}

.blog-post-link {
  display: block;
  margin-bottom: 2rem;
  transition: all 0.3s;
}

.blog-post-link div b {
  transition: all 0.3s;
}

.blog-post-link:hover div b {
  color: var(--color-text-primary);
}
</style>
