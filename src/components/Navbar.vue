<!-- -->
<template>
    <nav class="navbar navbar-expand"  
    :class="[`bg-${navTheme}`, `navbar-${navTheme}`]" 
        >
        <div class="container-fluid">
            <a class="navbar-brand" href="#">ALP</a>
            <ul class="navbar-nav">
               
                <li v-for="(page, index) in pages" class="nav-item" key="index">
                    <navbar-link
                        :page="pages[index]"
                        :isActive="activePage == index"
                        @click="navLinkClick(index)"
                    >

                    </navbar-link>
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
                        class="btn"
                        >{{ `${navTheme == 'light' ? 'dark' : 'light'} Mode` }}</button></li>
                    </ul>
                    </li>
            </ul>
        </div>
        </nav>
</template>
<style>
    .navbar img {
        width: 60px;
    }
    .navbar-brand {
        margin-left: 15px;
        font-weight: 700;
        font-size: 22px !important; 
    }
    .navbar {
        backdrop-filter: blur(7px);
        border-bottom-left-radius: 15px;
        border-bottom-right-radius: 15px;
        z-index: 3;
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
import NavbarLink from './NavbarLink.vue';

export default {
        components: {
        NavbarLink
        },
        props: ['pages', 'activePage','navLinkClick'],
        data() {
            return{
                navTheme:'dark'
            }
        }
}

</script>