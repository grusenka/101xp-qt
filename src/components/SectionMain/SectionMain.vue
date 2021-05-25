<template>
<Section class="section section-main">
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

    <footer class="section-main__footer">
        <action-link href="#character-section">
            Далее
        </action-link>
    </footer>
</Section>
</template>

<script>
import Section from '../Section/Section.vue';
import PlayButton from '../PlayButton/PlayButton.vue';
import ActionLink from '../ActionLink/ActionLink.vue';

export default {
  name: 'section-main',
  components: {
    Section,
    PlayButton,
    ActionLink,
  },
};
</script>

<style lang="scss" src="./SectionMain.scss" />
