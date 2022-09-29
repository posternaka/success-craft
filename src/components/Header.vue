<template>
    <div class="wrapper">
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

</style>