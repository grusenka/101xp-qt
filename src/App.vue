<template>
  <main class="landing">
    <section-main />

    <section-characters />

    <section-actions />
  </main>
</template>

<script>
import SectionMain from './components/SectionMain/SectionMain.vue';
import SectionCharacters from './components/SectionCharacters/SectionCharacters.vue';
import SectionActions from './components/SectionActions/SectionActions.vue';

export default {
  name: 'App',
  components: {
    SectionMain,
    SectionCharacters,
    SectionActions,
  },
};
</script>
