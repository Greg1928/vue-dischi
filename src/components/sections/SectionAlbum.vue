<template>
  <section>
      <div class="container">
          <div class="row">
              <CardAlbum class="col-12 col-sm-6 col-md-4 col-lg-2" v-for="(album, i) in albums" :key="i" :album="album"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import CardAlbum from '../commons/CardAlbum.vue';

export default {
    name: 'SectionAlbum',
    data(){
        return{
            albums: [],
        };
    },
    components:{
        CardAlbum,
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response;
        }).catch((err) => {
            console.log(err);
        });
    }
}
</script>

<style lang="scss" scoped>
section{
    background-color: var(--primary-color);
    height: calc(100vh - 80px);

    .row{
        padding-top: 60px;
    }
}
</style>