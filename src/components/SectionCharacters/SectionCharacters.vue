<template>
    <Section
        class="section section-character"
        :class="{'section-character_isolda': characterIndex === 0,
        'section-character_pamela': characterIndex === 1,
        'section-character_lleyn': characterIndex === 2}"
    >
        <template v-slot:header>
            <h2 class="section-character__title" id="character-section">
                Уникальные персонажи и сотни комбо
            </h2>
        </template>

        <div class="section-character__content">
            <div class="character-slider">
                <article class="character">
                    <div class="character__info">
                        <h3
                            class="character__name"
                            :class="{'character__name_isolda': characterIndex === 0,
                            'character__name_pamela': characterIndex === 1,
                            'character__name_lleyn': characterIndex === 2}"
                        >{{ values[characterIndex].Name }}</h3>

                        <p
                            class="character__fraction"
                            :class="{'character__fraction_isolda': characterIndex === 0,
                            'character__fraction_pamela': characterIndex === 1,
                            'character__fraction_lleyn': characterIndex === 2}"
                        >{{ values[characterIndex].Subtitle }}</p>

                        <p class="character__information">
                            {{ values[characterIndex].Information }}
                        </p>

                        <ul class="character__skill-list">
                            <li
                                v-for="skill in values[characterIndex].Skills"
                                :key="skill.ID"
                                class="character__skill-item"
                            >
                                <img
                                    class="character__skill-image"
                                    :src="skill.Skill.Image"
                                    alt="Умение героя"
                                />

                                <div class="character__skill-information">
                                    <h4 class="character__skill-title">{{ skill.Skill.Title }}</h4>

                                    <p class="character__skill-description">
                                        {{ skill.Skill.Information }}
                                    </p>
                                </div>
                            </li>
                        </ul>
                    </div>

                    <ul class="character__navigation">
                        <li class="character__navigation-item">
                            <character-button
                                class="character-button_icon_isolda"
                                :class="{active: characterIndex === 0}"
                                @click="isoldaSlideHandler"
                            >
                                Изольда
                            </character-button>
                        </li>
                        <li class="character__navigation-item">
                            <character-button
                                class="character-button_icon_pamela"
                                :class="{active: characterIndex === 1}"
                                @click="pamelaSlideHandler"
                            >
                                Памела
                            </character-button>
                        </li>
                        <li class="character__navigation-item">
                            <character-button
                                class="character-button_icon_lleyn"
                                :class="{active: characterIndex === 2}"
                                @click="lleynSlideHandler"
                            >
                                ЛЛейн
                            </character-button>
                        </li>
                    </ul>
                </article>

                <action-button
                    class="character-slider__previous action-button_icon_previous"
                    @click="previousSlideHandler"
                >
                    Предыдущий слайд
                </action-button>

                <action-button
                    class="character-slider__next action-button_icon_next"
                    @click="nextSlideHandler"
                >
                    Следующий слайд
                </action-button>
            </div>

            <p class="section-character__text">
              60&nbsp;наемников с&nbsp;неповторимой историей и&nbsp;сотни возможностей
              для посторения команды ждут<br/>тебя! Система всязей меджу
              персонажами&nbsp;&mdash; важная часть игрового сюжета и&nbsp;тонкий механизм<br/>
              настройки боевого отряда. Выбери совю фракцию и&nbsp;получай бонусык мощи!
            </p>
        </div>

        <footer class="section-character__footer">
            <action-link href="#actions-section">
                Далее
            </action-link>
        </footer>
    </Section>
</template>

<script>
import Section from '../Section/Section.vue';
import ActionButton from '../ActionButton/ActionButton.vue';
import CharacterButton from '../CharacterButton/CharacterButton.vue';
import ActionLink from '../ActionLink/ActionLink.vue';

export default {
  name: 'section-character',
  components: {
    Section,
    ActionButton,
    CharacterButton,
    ActionLink,
  },
  data() {
    return {
      characterIndex: 0,
      values: [
        /* eslint-disable global-require */
        {
          ID: '01',
          Name: 'Изольда королева холода',
          Subtitle: 'Империя бессметных',
          Information: 'Появление королевы холода и ее верного медведя предвещает ледяная буря. Неуязвимая Изольда замораживает противников насмерть и не знает пощады.',
          Skills: [
            {
              ID: '01',
              Skill: {
                Title: 'Конец зимы',
                Information: '360% урона авангарду врага',
                Image: require('../../assets/SkillIsolda1.png'),
              },
            },
            {
              ID: '02',
              Skill: {
                Title: 'Морозная ария',
                Information: 'Ледяной щит уменьшает получаемый урон на 20%',
                Image: require('../../assets/SkillIsolda2.png'),
              },
            },
          ],
        },
        {
          ID: '02',
          Name: 'Памела королева тьмы',
          Subtitle: 'Союз просвященных',
          Information: 'Памела супруга  древнего огненного дракона, одна из первых овладела магией. Никто не знает, на чьей стороне она сражается на самом деле.',
          Skills: [
            {
              ID: '01',
              Skill: {
                Title: 'Черное дыхание',
                Information: 'Наносит врагу с мин. ОЗ 426% урона',
                Image: require('../../assets/SkillPamela1.png'),
              },
            },
            {
              ID: '02',
              Skill: {
                Title: 'Проклятие дракона',
                Information: 'Проклинает всех врагов, снижая урон на 15%',
                Image: require('../../assets/SkillPamela2.png'),
              },
            },
          ],
        },
        {
          ID: '03',
          Name: 'ЛЛейн дикий клинок',
          Subtitle: 'Цитадель небожителей',
          Information: 'Зверолюд Ллейн выбрал кровавый путь наемного убийцы в тайной организации «Покров». Его прозвали «Дикий клинок» из-за его жестокости и скрости.',
          Skills: [
            {
              ID: '01',
              Skill: {
                Title: 'Дикий разрез',
                Information: 'Превращает 30% наносимого урона в ОЗ.',
                Image: require('../../assets/SkillLleyn1.png'),
              },
            },
            {
              ID: '02',
              Skill: {
                Title: 'Найти и уничтожить',
                Information: 'Наносит 313% урона врагу.',
                Image: require('../../assets/SkillLleyn2.png'),
              },
            },
          ],
        },
        /* eslint-enable global-require */
      ],
    };
  },
  methods: {
    previousSlideHandler() {
      const previousCharacter = this.characterIndex - 1;

      if (previousCharacter >= 0) {
        this.characterIndex = previousCharacter;
      } else {
        this.characterIndex = 2;
      }
    },

    nextSlideHandler() {
      const nextCharacter = this.characterIndex + 1;

      if (nextCharacter < 3) {
        this.characterIndex = nextCharacter;
      } else {
        this.characterIndex = 0;
      }
    },

    isoldaSlideHandler() {
      this.characterIndex = 0;
    },

    pamelaSlideHandler() {
      this.characterIndex = 1;
    },

    lleynSlideHandler() {
      this.characterIndex = 2;
    },
  },
};
</script>

<style lang='scss'>
@import './SectionCharacters.scss';
@import '../CharacterSlider/CharacterSlider.scss';
@import '../Character/Character.scss';

</style>
