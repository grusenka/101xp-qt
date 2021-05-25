<template>
<Section class="section section-mount" hasFooter="true">
    <template v-slot:header>
        <h2 class="section-mount__title">
            Многогранная прокачка
        </h2>
    </template>

    <div class="section-mount__content">
        <ul class="character-mount-list">
            <li class="character-mount-list__item">
                <h2 class="character-mount-list__rating">Боевой рейтинг 30 000</h2>
                <p class="character-mount-list__level">1 уровень</p>
            </li>

            <li class="character-mount-list__item">
                <h2 class="character-mount-list__rating">Боевой рейтинг 150 000</h2>
                <p class="character-mount-list__level">50 уровень</p>
            </li>
        </ul>

        <p class="section-mount__text">
            Пройди десятки элитных данжей, собери крепкие доспехи и&nbsp;сильнейшее
            оружие и&nbsp;приручи<br/>верных маунтов. Добывай ценные ресурсы для
            максимальной прокачки снаряжения и&nbsp;отряда:<br/>развивай скиллы,
            применяй древние кодексы и&nbsp;собирай уникальные комбинации!<br/>Выработай
            свою стратегию боя и&nbsp;выбери ключевые умения для победы над врагами!
        </p>
    </div>
</Section>
</template>

<script>
import Section from '../Section/Section.vue';

export default {
  name: 'section-mount',
  components: {
    Section,
  },
};
</script>

<style lang="scss">
@import "./SectionMount.scss";
@import "../CharacterMountList/CharacterMountList.scss";
</style>
