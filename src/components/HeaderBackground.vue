<template>
    <div class="container-fluid header-background">
        <h1>Welcome to ALP {{ page.pageTitle }}</h1>
    </div>
</template>

<style>
    .header-background {
        background: url('../assets/background.webp');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        width: 100vw;
        height: 50vh;
        transform: translateY(-20px);
        z-index: 0;
        border-bottom-left-radius: 15px;
        border-bottom-right-radius: 15px;
        display: flex;
        justify-content: center;
        align-items: center;
        
    }
    .header-background h1 {
        font-size: 40px;
        color: white;
        text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000, 1px 1px 0 #000;
    }
</style>
<script>
    export default {
        props:['page']
    }
</script>