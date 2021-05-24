<template>
  <main class="landing">
    <section-main />

    <section-characters />
  </main>
</template>

<script>
import SectionMain from './components/SectionMain/SectionMain.vue';
import SectionCharacters from './components/SectionCharacters/SectionCharacters.vue';

export default {
  name: 'App',
  components: {
    SectionMain,
    SectionCharacters,
  },
};
</script>
