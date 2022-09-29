<template>
    <div class="wrapper">
        <div class="container">
            <h3 class="title text-center">Applications</h3>
            <div class="applications_cards d-flex flex-row">
                <div class="card d-flex flex-column" v-for="n in 8" :key="n">
                    <img :src="require(`@/assets/img/applications/${n}.png`)" :alt="`App ${n}`">
                    <h5 class="card_title text-center">App {{n}}</h5>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'application_cards',
    }
</script>

<style scoped>
    .wrapper {
        color: #000;
        background-color: #F5F7FA;
        padding-bottom: 56px;
    }

    .title {
        font-size: 28px;
        padding: 44px 0 45px 0;
    }

    .applications_cards {
        column-gap: 96px;
        row-gap: 45px;
        flex-wrap: wrap;
    }

    .card {
        cursor: pointer;
    }

    .card_title {
        color: #fff;
        background-color: #3D3D3D;
    }

    h5 {
        margin: 0;
    }
</style>