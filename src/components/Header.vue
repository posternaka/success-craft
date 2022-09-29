<template>
    <div id="home" class="wrapper">
        <div class="container d-flex flex-column justify-content-center align-items-center">
            <h1>Welcome to Test Page</h1>
            <p>Front-end developer</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'welcome-information',
    };
</script>

<style scoped>
    .wrapper {
        height: 100%;
        background-image: url('@/assets/img/header/background-header.png');
        background-size: 100% 100%;
        background-repeat: no-repeat;
        color: #fff;
    }

    h1 {
        font-size: 4.3rem;
        line-height: 87.5px;
        font-weight: bold;
    }

    p {
        font-size: 2.3rem;
    }

    @media (max-width: 992px) {
        h1 {
            font-size: 4.0rem;
            margin-bottom: 10px;
        }
    }

    @media (max-width: 768px) {
        h1 {
            font-size: 3.0rem;
            margin-bottom: 10px;
        }
    }

    @media (max-width: 530px) {
        h1 {
            font-size: 2.0rem;
            margin-bottom: 10px;
        }

        p {
            font-size: 1.3rem;
        }
    }
</style>