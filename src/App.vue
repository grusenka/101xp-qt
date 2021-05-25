<template>
  <main class="landing">
    <section-main />

    <section-characters />

    <section-actions />

    <section-mount />

    <section-footer />
  </main>
</template>

<script>
import SectionMain from './components/SectionMain/SectionMain.vue';
import SectionCharacters from './components/SectionCharacters/SectionCharacters.vue';
import SectionActions from './components/SectionActions/SectionActions.vue';
import SectionMount from './components/SectionMount/SectionMount.vue';
import SectionFooter from './components/SectionFooter/SectionFooter.vue';

export default {
  name: 'App',
  components: {
    SectionMain,
    SectionCharacters,
    SectionActions,
    SectionMount,
    SectionFooter,
  },
};
</script>
