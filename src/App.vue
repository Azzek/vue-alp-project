<template>

    <navbar 
        :pages="pages"
        :active-page="activePage"
        :nav-link-click="(index) => activePage = index"
    ></navbar>

    <page-viewer
            :page="pages[activePage]">
    </page-viewer>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';
export default {
    components: {
        Navbar,
        PageViewer,
    },
    data() {
        return {
            activePage:0,
            pages: [
            {
                pageBtn:'Home',
                pageTitle:'Home page',
                PageContent:"Automotive Logistics Polska Sp. z o.o. was founded in October 2003 as a result of the experience and successes of stakeholders in the field of freight forwarding services, transportation, logistics management, accounting, marketing, administration and human resources. The company's success in the field of transport and logistics is also due to the fact that all the managers are university graduates in the field of transport. The staff are constantly improving their skills through participation in the thematic courses, among others Master Business of Administration. The company manegement operates on the basis of The Certificate of Professional Competence in International Transport.Initially we started with the provision of freight forwarding services, with time we bought our own cars, and now we have our own fleet with a capacity range of 1,5-24t. Currently the basic aim of the company is to create a group of carries that meet the most demanding quality requirements of corporate customers and logistic providers with the quality of their service, timeliness of delivery and the choice of the fleet. UwUUwU"
            },
            {
                pageBtn:'About',
                pageTitle:'About page',
                PageContent:'Welcome to About page UwU'
            },
            {
                pageBtn:'Contact',
                pageTitle:'Contact page',   
                PageContent:"tel: +48 32 / 214 90 29 fax: +48 32 / 214 90 30 UwU"
            },
            {
                pageBtn:'Offer',
                pageTitle:'Offer',   
                PageContent:"This is Offert page UwU"
            }
        ]
        };
    },
}
</script>