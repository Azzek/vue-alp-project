<template>
    <div class="container-fluid">

        <h1>{{ page.pageTitle }}</h1>
        <p> {{ page.PageContent }}</p>
    </div>
</template>

<script>
    export default {
        props: ['page'],
}
</script>