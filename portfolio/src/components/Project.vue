<template>
  <div>
    <h2>projetos</h2>
    <div class="projects-wrapper">
      <a
        href="https://time.rodrigoacs.com/"
        target="_blank"
      >
        <img
          src="https://github-readme-stats.vercel.app/api/pin?title_color=ffffff&amp;icon_color=9381ff&amp;text_color=d4d4d4&amp;bg_color=161616&amp;hide_border=true&amp;username=rodrigoacs&amp;locale=en&amp;show_icons=false&amp;repo=time-tracker&amp;description_lines_count=1"
        />
      </a>
      <a
        href="https://git-aesthetics.rodrigoacs.com/"
        target="_blank"
      >
        <img
          src="https://github-readme-stats.vercel.app/api/pin?title_color=ffffff&amp;icon_color=9381ff&amp;text_color=d4d4d4&amp;bg_color=161616&amp;hide_border=true&amp;username=rodrigoacs&amp;locale=en&amp;show_icons=false&amp;repo=git-aesthetics&amp;description_lines_count=1"
        />
      </a>
    </div>
  </div>
</template>
<script setup></script>
<style scoped>
.projects-wrapper {
  display: flex;
  gap: 1.6rem;
  justify-content: center;
}

img {
  width: auto;
  height: 120px;
}

h2 {
  margin-top: 1.6rem;
  margin-bottom: 0.8rem;
}

p {
  margin-bottom: 0.8rem;
}
</style>
