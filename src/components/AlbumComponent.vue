<template>
<div class="container" >
    <div v-for="(album, index) in albums" :key="index" class="card">
        <div>
            <img :src="album.poster" alt="">
        </div>
        <div class="descriptions">
            <p class="title">{{album.title}}</p>
            <p>{{album.author}}</p>
            <p>{{album.year}}</p>
        </div>        
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
.card{
    color: white;
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    padding: 20px;
    background-color: #303B46;
    width: calc(100% / 6);
}
.container{
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    padding: 100px;
}
.container img{
    width: 150px;
    display: block;
    height: 100%;
    padding-bottom: 10px;
}
.descriptions p{
    color: #616B75;
}
.descriptions .title{
    font-size: 20px;
    padding-bottom: 10px;
    color: white;
}


</style>