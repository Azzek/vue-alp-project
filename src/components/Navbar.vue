<!--:class="[`bg-${navTheme}`, `navbar-${navTheme}`]"  -->
<template>
    <nav class="navbar navbar-expand"  
    
        >
        <div class="container-fluid">
            <a><img  src="../assets/logo.png" alt="" ></a>
            <ul class="navbar-nav">
               
                <li v-for="(page, index) in pages" class="nav-item" key="index">
                    <a
                        href="#"
                        class="nav-link"
                        @click="navLinkClick(index)"
                        :class="{active: index == activePage}"
                        :title="`This link goes to the ${page.PageTitle}`"
                    >{{ page.pageBtn }}</a>
                </li>
                <li class="nav-item dropdown" >
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown"  data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Dropdown
                    </a>
                    <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                    <li><a class="dropdown-item" href="#">English Version</a></li>
                    <li><a class="dropdown-item" href="https://wizytowka.rzetelnafirma.pl/r/reportecr?banner=6t0twqe9">Download files</a></li>
                    <li><a class="dropdown-item" href="https://nbp-pl.translate.goog/statystyka-i-sprawozdawczosc/kursy/tabela-a/?_x_tr_sl=pl&_x_tr_tl=en&_x_tr_hl=pl">Rate of exchange</a></li>
                    <li><hr class="dropdown-divider"></li>
                    <li><button
                        @click="navTheme == 'light' ? navTheme = 'dark' : navTheme = 'light' "
                        class="btn">{{ `${navTheme == 'light' ? 'dark' : 'light'} Mode` }}</button></li>
                    </ul>
                    </li>
            </ul>
        </div>
        </nav>
</template>
<style>
    .navbar img {
        width: 60px;
        background-color: transparent;
    }
    .navbar {
        backdrop-filter: blur(7px);
        border-radius: 15px;
    }
    .dropdown-menu {
        left: -59px;
    }
    .nav-item a {
        font-weight: 600;
    }
    @media (max-width: 430px) { 
        .navbar img {
            width: 45px;
        } 
     }
    
</style>
<script>
export default {
        props: ['pages', 'activePage','navLinkClick'],
        data() {
            return{
                navTheme:'dark'
            }
        }
}

</script>