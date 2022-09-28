<template>
    <div class="wrapper" >
        <div class="container">
            <h3 class="frameworks_title">Frameworks</h3>
            <div class="cards d-flex flex-row" v-for="framework in frameworks" :key="framework.id">
                <div class="about-us">
                    <h3 class="about-us_title">{{framework.title}}</h3>
                    <p class="about-us_text">{{framework.text}}</p>
                    <a class="btn btn-primary" href="#" role="button">Read more</a>
                    <a class="btn btn-outline-primary" href="#" role="button">Contact us</a>
                </div>
                <div>
                    <img :src="require(`@/assets/img/frameworks/${framework.picture}.png`)" :alt="`${framework.title}`">
                </div>  
            </div>
        </div>
    </div>
</template>

<!-- <div class="card mb-3">
                <img src="../assets/img/applications/1.png" class="card-img-top" alt="">
                <div class="card-body">
                    <h5 class="card-title">Заголовок карточки</h5>
                    <p class="card-text">Это более широкая карточка с вспомогательным текстом ниже в качестве естественного перехода к дополнительному контенту. Этот контент немного длиннее.</p>
                    <p class="card-text"><small class="text-muted">Последнее обновление 3 мин. назад</small></p>
                </div>
            </div> -->

<script>
    export default {
        name: 'nav-bar',
        data() {
            return { frameworks:
                [{
                    "id": 1,
                    "picture": "vue",
                    "title": "Vue js",
                    "text": "Vue.js is an open source JavaScript framework for creating user interfaces. It is easily integrated into projects using other JavaScript libraries. It can function as a web framework for developing single-page applications in a reactive style."
                },
                {
                    "id": 2,
                    "picture": "react",
                    "title": "React js",
                    "text": "React is an open source JavaScript library for developing user interfaces. instagram facebook react is developed and supported by a community of individual developers and corporations. React cam be used to develop single-page and mobile applications."
                },
                {
                    "id": 3,
                    "picture": "angular",
                    "title": "Angular js",
                    "text": "AngularJS is an open source JavaScript framework. Designed for the development of single-page applications. It's goal is to expand browser applications based on the MVC template, as well as simplify testing and development."
                },]
            }
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
    }

    .cards {
        background-color: #fff;
        gap: 62px;
        border-radius: 15px;
        margin-bottom: 45px;
    }

    .about-us {
        padding: 25px 11px;
    }

    .about-us_title {
        margin-bottom: 16px;
        font-size: 28px;
    }

    .about-us_text {
        margin-bottom: 28px;
        color: #808080;
    }
</style>