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
    height: 80px;

    img{
       height: 3rem;
       margin: 1rem;
    }
}
</style>