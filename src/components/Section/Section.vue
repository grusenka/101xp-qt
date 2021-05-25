<template>
    <section class="section">
        <header><slot name="header"/></header>

        <slot/>
    </section>
</template>

<script>

export default {
  name: 'section',
};
</script>
