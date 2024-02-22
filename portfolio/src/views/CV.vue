<template>
  <div>
    <h2 class="header">Rodrigo Augusto Correa Soares</h2>
    <p class="socials">
      <span> {{ $t("cv.birthDate") }}</span>
    </p>
    <p class="socials">
      <span> {{ $t("cv.home") }}</span>
    </p>
    <p class="socials">
      <a
        target="_blank"
        href="mailto:rodrigohths@gmail.com"
      >rodrigohths@gmail.com</a>
      <a
        target="_blank"
        href="https://github.com/rodrigoacs"
      >&nbsp;|&nbsp;GitHub&nbsp;|&nbsp;</a>
      <a
        target="_blank"
        href="https://www.linkedin.com/in/rodrigoacsoares/"
      > LinkedIn | </a>
      <a
        target="_blank"
        href="https://rodrigoacs.com"
      >&nbsp;Site</a>
    </p>

    <h3>{{ $t("cv.resume") }}</h3>
    <p> {{ $t("cv.resumeText") }} </p>

    <h3> {{ $t("cv.education") }} </h3>

    <!-- <div
      v-for='(edu, index) in $t("cv.educations")'
      :key='index'
    >
      <p>{{ edu }}</p>
      <p>{{ education.local }}</p>
      <p>{{ education.course }}</p>
    </div> -->

    <div>
      <p>{{ $t("cv.educations[0].time") }}</p>
      <p>{{ $t("cv.educations[0].local") }}</p>
      <p>{{ $t("cv.educations[0].course") }}</p>
    </div>
    <br>
    <div>
      <p>{{ $t("cv.educations[1].time") }}</p>
      <p>{{ $t("cv.educations[1].local") }}</p>
      <p>{{ $t("cv.educations[1].course") }}</p>
    </div>

    <h3>{{ $t("cv.experience") }}</h3>
    <div>
      <p> {{ $t("cv.experienceText[0].time") }} </p>
      <p> {{ $t("cv.experienceText[0].title") }} </p>
      <p> {{ $t("cv.experienceText[0].description") }} </p>
    </div>

    <h3> {{ $t("cv.skills") }} </h3>
    <p>&gt; {{ $t("cv.skills1") }}</p>
    <p>&gt; {{ $t("cv.skills2") }}</p>
    <p>&gt; {{ $t("cv.skills3") }}</p>
    <p>&gt; {{ $t("cv.skills4") }}</p>
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
