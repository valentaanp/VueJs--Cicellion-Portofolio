<script setup>
import HeaderTitle from '@/components/HeaderTitle.vue';
import ProjectLists from '@/components/ProjectCards.vue';
</script>

<template>
  <!-- Start Section Projects -->
  <kinesis-container tag="section" class="projects" id="projectSection">
    <!-- Pattern Group -->
    <div class="pattern">
      <kinesis-element :strength="-50" class="ornament ornament__ellipse-1"></kinesis-element>
    </div>

    <!-- Content -->
    <div class="container">
      <div class="header">
        <HeaderTitle titleMsg="Projects" />
        <p class="text-md" v-motion-slide-visible-once-top>These are some samples of the work I've done so far.</p>
      </div>
      <ProjectLists classProp="project-list--short" />
      <router-link class="btn btn--md btn--tertiary" v-motion-slide-visible-once-bottom to="/project">
        <p>See More</p>
      </router-link>
    </div>
  </kinesis-container>
  <!-- End Section Projects -->
</template>

<style lang="scss" scoped>
@import '@/assets/scss/styles.scss';

section.projects#projectSection {
  height: 1338px;

  @include media-breakpoint-down(lg) {
    height: auto;
  }
  // Pattern Settings
  .pattern {
    .ornament__ellipse-1 {
      width: 291px;
      height: 291px;
      left: -121px;
      top: 1097px;
      background: #0354e2;
    }
  }
  .container {
    display: flex;
    flex-direction: column;
    gap: toRem(32);
    align-items: center;

    .btn {
      @include media-breakpoint-down(xs-2) {
        width: 100%;
      }
    }
  }
}
</style>
