<template>
    <div class="navigation">
        <nav class="navbar fixed-top bg-light">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logo.svg" alt="Company's logo">
                </a>
                <ul class="nav justify-content-end">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">HOME</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">ABOUT US</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">FRAMEWORKS</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">APPLICATIONS</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">CONTACT US</a>
                    </li>
                </ul>
            </div>
        </nav>
    </div>
</template>

<script>
    export default {
        name: 'nav-bar',
    };
</script>

<style scoped>
    .container {
        padding-left: 0;
        padding-right: 0;
    }
    .navigation {
        max-height: 80px;
        font-family: 'Roboto', sans-serif;
    }

    nav {
        padding: 16px 0;
        font-size: 1.1rem;
    }

    a {
        color: #000;
    }
</style>