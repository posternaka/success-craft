<template>
    <div id="frameworks" class="wrapper" >
        <div class="container">
            <h3 class="frameworks_title">Frameworks</h3>
            <div class="cards d-flex flex-row" v-for="framework in DATA_OF_FRAMEWORKS" :key="framework.id">
                <div class="about-us d-flex flex-column justify-content-between">
                    <div>
                        <h3 class="about-us_title">{{framework.title}}</h3>
                        <p class="about-us_text">{{framework.text}}</p>
                    </div>
                    <div>
                        <a class="btn btn-primary" href="#" role="button">Read more</a>
                        <a class="btn btn-outline-primary" href="#" role="button">Webinar</a>
                    </div>
                </div>
                <img class="img-responsive" :src="require(`@/assets/img/frameworks/${framework.picture}.png`)" :alt="`${framework.title}`">
            </div>
        </div>
    </div>
</template>

<script>
    import { DATA_OF_FRAMEWORKS } from '../data/data';

    export default {
        name: 'nav-bar',
        data() {
            return { DATA_OF_FRAMEWORKS }
        },
    };
</script>

<style scoped>
    .wrapper {
        color: #000;
        text-align: left;
        padding-bottom: 16px;
        background-color: #F5F7FA;
    }

    .frameworks_title {
        font-size: 28px;
        text-align: center;
        padding: 44px 0 45px 0;
        font-weight: bold;
    }

    .cards {
        background-color: #fff;
        gap: 62px;
        border-radius: 15px;
        margin-bottom: 45px;
        overflow: hidden;
    }

    .cards:nth-child(2n){
        flex-direction: row-reverse !important;
    }

    .about-us {
        padding: 25px 11px;
    }

    .about-us a:first-of-type {
        margin-right: 25px;
    }

    .about-us_title {
        margin-bottom: 16px;
        font-size: 24px;
        font-weight: bold;
    }

    .about-us_text {
        margin-bottom: 28px;
        color: #808080;
    }

    @media (max-width: 1400px) {
        .about-us a:first-of-type {
            margin-right: 10px;
        }
    }

    @media (max-width: 1200px) {
        .about-us a:first-of-type {
            margin-bottom: 15px;
            margin-right: 0;
        }
    }

    @media (max-width: 992px) {
        .about-us_title {
            margin-bottom: 12px;
            font-size: 20px;
            font-weight: bold;
        }

        .about-us_text {
            font-size: 0.8rem;
            margin-bottom: 22px;
            color: #808080;
        }

        .cards {
            gap: 30px;
        }

        img {
            width: 50%;
            height: auto;
        }
    }

    @media (max-width: 768px) {
        .cards {
            gap: 15px;
        }

        img {
            width: 50%;
            height: auto;
        }

        .btn {
            width: 160px;
            height: 40px;
        }
    }
</style>