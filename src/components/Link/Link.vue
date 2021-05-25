<template>
<a class="link" :href="href"><slot/></a>
</template>

<script>
export default {
  name: 'link',
};
</script>

<style lang="scss" src="./Link.scss" />
