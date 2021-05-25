<template>
  <main class="landing">
    <section-main />

    <section-characters />

    <section-actions />

    <section-mount />
  </main>
</template>

<script>
import SectionMain from './components/SectionMain/SectionMain.vue';
import SectionCharacters from './components/SectionCharacters/SectionCharacters.vue';
import SectionActions from './components/SectionActions/SectionActions.vue';
import SectionMount from './components/SectionMount/SectionMount.vue';

export default {
  name: 'App',
  components: {
    SectionMain,
    SectionCharacters,
    SectionActions,
    SectionMount,
  },
};
</script>
