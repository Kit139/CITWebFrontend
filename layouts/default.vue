<template>
<!DOCTYPE html>
<html lang="zh-cmn-Hans">




<body class="{% if page.url == "/" %} homefirstpage {% endif %}">

    <!-- Navbar -->
    <nav id="MagicMenu" class="topnav navbar navbar-expand-lg navbar-light bg-white fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#"><strong>CitWeb</strong></a>
            <button class="navbar-toggler collapsed" type="button" data-toggle="collapse" data-target="#navbarColor02"
                aria-controls="navbarColor02" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="navbar-collapse collapse" id="navbarColor02" style="#">
                <ul class="navbar-nav mr-auto d-flex align-items-center">
                    <!-- {% include menu-header.html %} -->
                    <!-- <MenduHeader /> -->
                    <li class="nav-item">
                        <a class="nav-link" href="/">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/authors-list">Authors</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/contact">Contact</a>
                    </li>
                    <li class="nav-item">
                        <a target="_blank" class="nav-link" href="https://www.wowthemes.net/themes/mundana-wordpress/">WP</a>
                    </li>
                    <li class="nav-item">
                        <a target="_blank" class="nav-link" href="https://www.wowthemes.net/themes/mundana-ghost/">Ghost</a>
                    </li>
                    <li class="nav-item">
                        <a target="_blank" class="nav-link" href="https://www.wowthemes.net/donate/">Buy me a coffee <i
                                class="fa fa-coffee text-danger"></i></a>
                    </li>
                </ul>
                <ul class="navbar-nav ml-auto d-flex align-items-center">
                    <!-- {% include search-lunr.html %} -->
                    <SearchLunr />
                </ul>
            </div>
        </div>
    </nav>

    <!-- Search Results -->
    <div id="lunrsearchresults">
        <ul class="mb-0"></ul>
    </div>

    <!-- Content -->
    <main role="main" class="site-content">
        <nuxt/>
    </main>


    <!-- Scripts: popper, bootstrap, theme, lunr -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.6/umd/popper.min.js"
        integrity="sha384-wHAiFfRlMFy6i5SRaxvfOCifBUQy1xHdJ/yoi7FRNXMRBu5WHdZYu1hA6ZOblgut"
        crossorigin="anonymous"></script>

    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/js/bootstrap.min.js"
        integrity="sha384-B0UglyR+jN6CkvvICOB2joaf5I4l3gm9GU6Hc1og6Ls7i6U/mkkaduKaBhlAXv9k"
        crossorigin="anonymous"></script>

    <script src="/assets/js/theme.js"></script>


    <!-- Footer -->
    <footer class="bg-white border-top p-3 text-muted small">
        <div class="container">
            <div class="row align-items-center justify-content-between">
                <div>
                    <span class="navbar-brand mr-2 mb-0"><strong>CitWeb</strong></span>
                    <span>Copyright ©
                        <script>document.write(new Date().getFullYear())</script>.</span>

                    <!--  Github Repo Star Btn-->
                    <a class="text-dark ml-1" target="_blank"
                        href="https://github.com/wowthemesnet/mundana-theme-jekyll"><i class="fab fa-github"></i> Fork
                        on Github</a>

                </div>
                <div>
                    Made with <a target="_blank" class="text-dark font-weight-bold"
                        href="https://www.wowthemes.net/mundana-jekyll-theme/"> Mundana Jekyll Theme </a> by <a
                        class="text-dark" target="_blank" href="https://www.wowthemes.net">WowThemes</a>.
                </div>
            </div>
        </div>
    </footer>

    <!-- {% include tracking-footer.html %} -->

</body>

</html>
</template>

<script>
// import MenduHeader from "../components/Menuheader"
import SearchLunr from "../components/Search-lunr"
export default {
    components:{
      // MenduHeader,
      SearchLunr
    }
}
</script>