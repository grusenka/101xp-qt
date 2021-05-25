<template>
    <Section class="section section-actions" hasFooter="true">
        <template v-slot:header>
            <h2 class="section-actions__title">
                Многочисленные PVP- и PVE-события
            </h2>
        </template>

        <div class="section-actions__content">
            <div
                class="section-actions__video"
                :class="{'section-actions__video_off': showPlayButton}"
            >
                <video loop ref="video">
                    <source src="../../assets/SectionActions__Video.mp4"/>
                </video>

                <button
                    v-if="showPlayButton"
                    class="section-actions__video-play"
                    @click="playVideoHandler"
                >
                    Просмотр
                </button>
            </div>

            <p class="section-actions__text">
                Стань самым сильным в&nbsp;турниарх и&nbsp;накажи противников
                в&nbsp;других серверов в&nbsp;кросс-серверных сражениях.<br/>
                Занимай места в&nbsp;PvP- и&nbsp;PvE-топах и&nbsp;получай
                эксклюзивные наргады и&nbsp;доструп к&nbsp;магазинам для избранных!
            </p>
        </div>
    </Section>

</template>

<script>
import Section from '../Section/Section.vue';

export default {
  name: 'section-actions',
  components: {
    Section,
  },
  data() {
    return {
      showPlayButton: true,
    };
  },
  methods: {
    playVideoHandler() {
      this.$refs.video.play();
      this.showPlayButton = false;
    },
  },
};
</script>

<style lang="scss" src="./SectionActions.scss" />
