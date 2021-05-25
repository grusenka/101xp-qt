<template>
    <a class="action-link" :href="href"><slot /></a>
</template>

<script>
export default {
  name: 'action-link',
  props: ['href'],
};
</script>

<style lang="scss" src="./ActionLink.scss"/>
