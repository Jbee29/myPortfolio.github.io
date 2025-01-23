<script setup>
  import { defineAsyncComponent } from 'vue';
  import LoadingSpinner from '@/components/LoadingSpinner.vue';

  //Import Components Asynchronously
  const Navbar = defineAsyncComponent(() => import('@/components/Navbar.vue'));
  const FrontSection = defineAsyncComponent(() => import('@/components/FrontSection.vue'));
  const AboutSection = defineAsyncComponent(() => import('@/components/AboutSection.vue'));
  const ExperienceSection = defineAsyncComponent(() => import('@/components/ExperienceSection.vue'));
  const ProjectSection = defineAsyncComponent(() => import('@/components/ProjectSection.vue'));
  const ContactSection = defineAsyncComponent(() => import('@/components/ContactSection.vue'));
  const FooterSection = defineAsyncComponent(() => import('@/components/FooterSection.vue'));
  const BackToTop = defineAsyncComponent(() => import('@/components/BackToTop.vue'));

</script>

<style>
  *{
    scrollbar-width: thin;
    scrollbar-color: #111827 #F1F1F1;
  }
</style>

<template>
  <div class="bg-black min-h-screen">
    <!-- Wrapping components in suspense to handle loading -->
    <Suspense>
      <template #default>
        <!-- Wrap all components inside a single root element -->
        <div>
          <Navbar />
          <FrontSection />
          <AboutSection />
          <ExperienceSection />
          <ProjectSection />
          <ContactSection />
          <FooterSection />
          <BackToTop />
        </div>
      </template>
      <template #fallback>
        <div class="flex justify-center items-center min-h-screen">
          <LoadingSpinner />
        </div>
      </template>
    </Suspense>
  </div>
</template>
