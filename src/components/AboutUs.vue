<template>
    <div id="about" class="wrapper">
        <div class="container d-flex flex-row">
            <div class="about-us d-flex flex-column justify-content-between">
                <div>
                    <h3 class="title">About us</h3>
                    <p class="text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset.</p>
                </div>
                <div>
                    <a class="btn btn-primary" href="#" role="button">Read more</a>
                    <a class="btn btn-outline-primary" href="#" role="button">Contact us</a>                    
                </div>
            </div>
            <img src="@/assets/img/about-us/top5-frontend-frameworks.png" alt="Top 5 frontend frameworks">
        </div>
    </div>
</template>

<script>
    export default {
        name: 'about-us',
    };
</script>

<style scoped>
    .wrapper {
        background-image: url('@/assets/img/about-us/background-about-us.png');
        background-size: 100% 100%;
        background-repeat: no-repeat;
        color: #000;
        text-align: left;
        padding: 90px 0;
    }

    .container {
        gap: 40px;
    }

    .title {
        margin-bottom: 16px;
        font-size: 28px;
        font-weight: bold;
    }

    .text {
        margin-bottom: 28px;
        color: #808080;
    }

    .about-us a:first-of-type {
        margin-right: 25px;
    }

    @media (max-width: 1200px) {
        .about-us a:first-of-type {
            margin-bottom: 15px;
            margin-right: 0;
        }
    }

    @media (max-width: 992px) {
        img {
            width: 50%;
            height: 70%;
            margin: auto;
        }
    }

    @media (max-width: 768px) {
        .title {
            margin-bottom: 12px;
            font-size: 20px;
            font-weight: bold;
        }

        .text {
            margin-bottom: 20px;
            font-size: 0.8rem;
        }
    }

    @media (max-width: 576px) {
        img {
            width: 40%;
            height: 50%;
            margin: auto;
        }
    }
</style>