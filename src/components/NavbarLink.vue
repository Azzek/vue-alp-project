<template>
    <a
        href="#"
        class="nav-link"
        :class="activeClasses"
        :title="`This link goes to the ${page.pageName}`"
    >{{ page.pageBtn }}</a>
</template>
<script>
    export default {
        props:['page', 'isActive'],
        computed: {
            activeClasses() {
                return {
                    emphasize: this.isActive,
                    active: this.isActive
                };
            }
        }
    }
</script>
<style>
.emphasize {
    text-decoration: underline !important;
}
</style>