<template>
    <section class="section">
        <header><slot name="header"/></header>

        <slot/>

        <footer v-if="hasFooter" class="section__footer">
            <action-button class="action-button_icon_next-section">Далее</action-button>
        </footer>
    </section>
</template>

<script>
import ActionButton from '../ActionButton/ActionButton.vue';

export default {
  name: 'section',
  props: ['hasFooter'],
  components: {
    ActionButton,
  },
};
</script>

<style lang="scss" src="./Section.scss"/>
