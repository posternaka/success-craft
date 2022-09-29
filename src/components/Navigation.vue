<template>
    <div class="navigation">
        <nav class="navbar bg-light">
            <div class="container">
                <a class="navbar-brand" href="#home">
                    <img src="../assets/img/logo.svg" alt="Company's logo">
                </a>
                <ul class="nav justify-content-end">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#home">HOME</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">ABOUT US</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#frameworks">FRAMEWORKS</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#applications">APPLICATIONS</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">CONTACT US</a>
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

    @media (max-width: 992px) {
        .navbar-brand {
            display: none;
        }
    }

    @media (max-width: 768px) {
        nav {
            padding: 8px 0;
            font-size: 0.8rem;
        }
    }
</style>