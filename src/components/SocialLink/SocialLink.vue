<template>
<a class="social-link" :href="href"><slot /></a>
</template>

<script>
export default {
  name: 'social-link',
  props: ['href'],
};
</script>

<style lang="scss" src="./SocialLink.scss"/>
