<template>
<Section class="section section-footer">
    <template v-slot:header>
        <h2 class="section-footer__title">
            Этот мир на грани разрушения. Но мы будем сражаться за него!
        </h2>
    </template>

    <div class="section-footer__content">
        <play-button class="section-footer__button"/>

        <p class="section-footer__text">
            Поделись странице в социальной сети
        </p>

        <ul class="social-link-list">
            <li class="social-link-list__item">
                <social-link class="social-link_facebook" href="#">Facebook</social-link>
            </li>

            <li class="social-link-list__item">
                <social-link class="social-link_vk" href="#">Вконтакте</social-link>
            </li>

            <li class="social-link-list__item">
                <social-link class="social-link_ok" href="#">Одноклассники</social-link>
            </li>

            <li class="social-link-list__item">
                <social-link class="social-link_mail" href="#">Mail</social-link>
            </li>
        </ul>

        <p class="section-footer__agreement">
            Нажимая кнопку «Играть», вы подтверждаете, что принимаете условия<br/>
            <Link href="#">Пользовательского соглашения</Link> и
            <Link href="#">Политики приватности</Link>.
        </p>

        <p class="section-footer__copyright">
            <img class="1section-footer__logo" src="../../assets/101xpLogo.png" alt="101xp.com"/>
        </p>
    </div>
</Section>
</template>

<script>
import Section from '../Section/Section.vue';
import PlayButton from '../PlayButton/PlayButton.vue';
import SocialLink from '../SocialLink/SocialLink.vue';
import Link from '../Link/Link.vue';

export default {
  name: 'section-footer',
  components: {
    Section,
    PlayButton,
    SocialLink,
    Link,
  },
};
</script>

<style lang="scss">
@import "./SectionFooter.scss";
@import "../SocialLinkList/SocialLinkList.scss"
</style>
