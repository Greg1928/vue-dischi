<template>
  <div class="album">
      <img :src="album.poster" :alt="album.title">
      <h5>{{album.title}}</h5>
      <div class="author">{{album.author}}</div>
      <div class="year">{{album.year}}</div>
  </div>
</template>

<script>
export default {
    name: 'CardAlbum',
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
.album{
    text-align: center;
    background-color: var(--secondary-color);
    margin: 10px 20px;
    img{
        max-width: 100%;
        padding: 15px;
    }
    h5{
        text-transform: uppercase;
        color: white;
        margin-bottom: 15px;
    }
    .author, .year{
        color: #808080;
    }
    .year{
        margin-bottom: 10px;
    }
}

</style>