<template>
<div class="container" >
    <div v-for="(album, index) in albums" :key="index" class="card">
        <img :src="album.poster" alt="">
        {{album.title}}
    </div>
</div>
   
</template>

<script>
import axios from 'axios'

export default {
    name: 'AlbumVue',
    data() { return{
        albums: []
    }       
    },
    methods: {
        callAlbums: function(){
           axios.get('https://flynn.boolean.careers/exercises/api/array/music') 
           .then(res =>{
               this.albums = res.data.response

           } )
        }
    },
    created(){
        this.callAlbums()
    }
}
</script>

<style scoped>
div{
    color: black;
}
.card{
    display: flex;
    flex-direction: column;
    align-items: center;
}
.container{
    display: flex;
    flex-wrap: wrap;
}
.container img{
    width: 200px;
    display: block;
    height: 100%;
}

</style>