<template>

    <navbar
        v-if="pages.length > 0"
        :pages="pages"
        :active-page="activePage"
        :nav-link-click="(index) => activePage = index"
    ></navbar>

    <HeaderBackground
        v-if="pages.length > 0"
        :page="pages[activePage]">
    >
    
    </HeaderBackground>
  <!--  <page-viewer
      :page="pages[activePage]">
    </page-viewer>
    -->
    <HomePage
        v-if="pages.length > 0 && pages[activePage].pageName == 'Home'"
        :page="pages[activePage]"
    >
    </HomePage>
   
</template>
<style>
.displayNone {
    display: none;
}
</style>
<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';
import HeaderBackground from './components/HeaderBackground.vue';
import HomePage from './components/HomePage.vue';
export default {
    components: {
        Navbar,
        PageViewer,
        HeaderBackground,
        HomePage,
    },
    created() {
        this.getPages()
    },
    data() {
        return {
            activePage:0,
            pages:[]
        };
    },
    methods: {
        async getPages() {
            let res = await fetch ('pages.json')
            let data = await res.json()

            this.pages = data;
            return data;
        }
    }
}
</script>