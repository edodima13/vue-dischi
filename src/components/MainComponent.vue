<template>
    <main>
        <section>
            <AlbumVue/>
        </section>
    </main>
</template>
<script>
import AlbumVue from './AlbumComponent.vue'

export default {
    name: 'MainVue',

    components: {
        AlbumVue
    }
}
</script>
<style scoped>

main{
    background-color: #1B2735;
}



</style>