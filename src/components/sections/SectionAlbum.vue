<template>
  <section>
      <div class="container">
          <h4>Select Genres</h4>
          <SelectOptions/>
          <div class="row">
              <CardAlbum class="col-12 col-sm-6 col-md-4 col-lg-2" v-for="(album, i) in genreFiltered" :key="i" :album="album"/>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';
import CardAlbum from '../commons/CardAlbum.vue';
import dataShared from '../../shared/dataShared';
import SelectOptions from '../commons/SelectOptions.vue';

export default {
    name: 'SectionAlbum',
    data(){
        return{
            dataShared,
            albums: [],
        };
    },
    components:{
        CardAlbum,
        SelectOptions
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response;
        }).catch((err) => {
            console.log(err);
        });
    },
    computed:{
        genreFiltered(){
            if(this.dataShared.SelectOption === 'All'){
                return this.albums;
            }else{
            return this.albums.filter((elm)=>{
                return elm.genre.toLowerCase() === (this.dataShared.SelectOption.toLowerCase());
            });
            }
        }
    }
}

</script>

<style lang="scss" scoped>
section{
    background-color: var(--primary-color);
    height: calc(100vh - 80px);
    overflow: auto;
    .container{
        padding-top: 20px;
    }

    .row{
        padding: 38px 0;
        justify-content: center;
    }
    h4{
        color: white;
        text-align: center;
    }
}
</style>