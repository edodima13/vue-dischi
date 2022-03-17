<template>
    <header>
        <div class="header-top">
        </div>
        <div class="header-main">
            <img src="../assets/logo-small.svg" alt="">
        </div>
        
    </header>
</template>
<script>


export default {
    name: 'HeaderVue'
}
</script>
<style scoped>
    .header-top{
        padding: 5px;
        border-top-left-radius: 5px;
        border-top-right-radius: 5px;
        width: 100%;
        background-color: #06090c;
    }

    .header-main{
        background-color: #2B323D;
    }
    img{
        width: 30px;
        margin: 10px 10px;
    }
</style>
