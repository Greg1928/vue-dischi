<template>
  <header>
      <img src="../../assets/img/spotify-logo.png" alt="Spotify Logo">
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>

<style lang="scss" scoped>
header{
    background-color: var(--secondary-color);

    img{
       height: 4rem;
       margin: 1.3rem;
    }
}
</style>