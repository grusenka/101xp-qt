<template>
<Section class="section section-main" hasFooter="true">
    <template v-slot:header>
        <h1 class="section-main__logo">Лига ангелов 2</h1>

        <h2 class="section-main__title">
            Возглавь непобедимую армию и спаси мир. В бесплатной браузерной MMORPG!
        </h2>
    </template>

    <div class="section-main__content">
        <play-button class="section-main__button"/>

        <p class="section-main__text">
            Судьба палнеты агнелов в твоих руках! Древнее зло выравалось
            из глубины <br/> преисподней, и лишь вмешательство героя спасет этот мир!<br/>
            Все зависит только от твоих решений!
        </p>
    </div>
</Section>
</template>

<script>
import Section from '../Section/Section.vue';
import PlayButton from '../PlayButton/PlayButton.vue';

export default {
  name: 'section-main',
  components: {
    Section,
    PlayButton,
  },
};
</script>

<style lang="scss" src="./SectionMain.scss" />
