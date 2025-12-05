<script setup>
    defineProps(["imagem"]);
</script>

<template>
    <div class="card">
        <button>💖</button>
        <img :src="imagem" alt="luar"/>
    </div>
</template>

<style scoped lang="scss">
.card {     
    width: 30vw;
    height: 50vh;
    position: relative;
    img{
        border-radius: 10px;    
        width: 70%;
        height: 70%;
    }

    button{
        position:absolute;
        background-color: transparent;
        border: none;

    }
}

</style>