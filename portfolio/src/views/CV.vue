<template>
  <div>
    <h2 class="header">
      Rodrigo Augusto Correa Soares
    </h2>

    <p class="socials">
      <span>
        {{ $t("cv.birthDate") }}
      </span>
    </p>

    <p class="socials">
      <span>
        {{ $t("cv.home") }}
      </span>
    </p>

    <p class="socials">
      <a
        target="_blank"
        href="mailto:rodrigohths@gmail.com"
      >
        rodrigohths@gmail.com
      </a>

      <a
        target="_blank"
        href="https://github.com/rodrigoacs"
      >
        &nbsp;|&nbsp;GitHub&nbsp;|&nbsp;
      </a>

      <a
        target="_blank"
        href="https://www.linkedin.com/in/rodrigoacsoares/"
      >
        LinkedIn |
      </a>

      <a
        target="_blank"
        href="https://rodrigoacs.com"
      >
        &nbsp;Site
      </a>
    </p>

    <h3>
      {{ $t("cv.resume") }}
    </h3>

    <p>
      {{ $t("cv.resumeText") }}
    </p>

    <h3>
      {{ $t("cv.education") }}
    </h3>

    <div
      v-for='(edu, index) in $tm("cv.educations")'
      :key='index'
    >
      <p>
        {{ edu.time }}
      </p>

      <p>
        {{ edu.local }}
      </p>

      <p>
        {{ edu.course }}
      </p>

      <br>
    </div>

    <h3>
      {{ $t("cv.experience") }}
    </h3>

    <div v-for='(exp, index) in $tm("cv.experiences")'>
      <p>
        {{ exp.time }}
      </p>

      <p>
        {{ exp.title }}
      </p>

      <p>
        {{ exp.description }}
      </p>

      <br>
    </div>

    <h3>
      {{ $t("cv.skills") }}
    </h3>

    <p>
      &gt; {{ $t("cv.skills1") }}
    </p>

    <p>
      &gt; {{ $t("cv.skills2") }}
    </p>

    <p>
      &gt; {{ $t("cv.skills3") }}
    </p>

    <p>
      &gt; {{ $t("cv.skills4") }}
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
h3 {
  margin-top: 2rem;
}

.header {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
  margin-top: 2rem;
}

div a,
div li {
  color: var(--color-text-secondary);
}

.socials {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  text-align: justify;
  color: var(--color-text-secondary);
}
</style>
