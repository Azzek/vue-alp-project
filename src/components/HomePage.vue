<template>
    <div id="home-container" class="container-fluid">
        <div>
            <section id="home" class="py-5">
            <div class="container" >
                <div class="row d-flex align-content-center justify-content-center">
                <div class="col-md-6">
                    <h1 class="display-4">Witaj w ALP Polska</h1>
                    <p class="lead">
                    {{ page.pageContent }}
                    </p>
                    <p>
                        {{page.pageDescription}}
                    </p>
                    <p>
                    Skontaktuj się z nami, aby dowiedzieć się więcej o naszych usługach i znaleźć
                    optymalne rozwiązania logistyczne dla Twojej firmy.
                    </p>
                </div>
                <div class="col-md-5">
                    <!-- Miejsce na zdjęcie/grafikę -->
                    <img
                    src="https://images.unsplash.com/photo-1616432043562-3671ea2e5242?q=80&w=1374&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" 
                    alt="Transportation Image"
                    class="img-fluid rounded image"
                    />
                </div>
                </div>
            </div>
            </section>
        </div>
    </div>
</template>
<style>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        
    }
    #home-container {
        background-color: whitesmoke;
        border-radius: 20px;
    }
</style>
<script>
    export default {
        props:['page'],
    }
</script>
