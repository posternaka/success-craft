<template>
    <div class="wrapper">
        <div class="container d-flex flex-row">
            <div class="faq_card d-flex flex-row">
                <img src="@/assets/img/faq/meeting.png" class="img-fluid"  alt="Picture about meeting">
                <div class="faq_info">
                    <h3 class="faq_title">Setup a Meeting</h3>
                    <p class="faq_text">Fill out our contact form and have someone get back to you within 24 hours.</p>
                    <a class="btn btn-primary" href="#" role="button">Schedule a Meeting</a>
                </div>
            </div>
            <div class="faq_card d-flex flex-row">
                <img src="@/assets/img/faq/ask.png" class="img-fluid" alt="Picture about ask">
                <div class="faq_info">
                    <h3 class="faq_title">Ask a Question</h3>
                    <p class="faq_text">Have a question? Just fill out our contact us form and we will get back to you.</p>
                    <a class="btn btn-primary" href="#" role="button">Ask a Question</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'faq_block',
    }
</script>

<style scoped>
    .wrapper {
        background-color: #fff;
        color: #000;
        text-align: left;
    }

    
    .faq_info {
        padding: 26px 20px;
    }
    
    .faq_title {
        font-size: 24px;
        font-weight: bold;
        margin-bottom: 10px;
    }
    
    .faq_text {
        color: #808080;
        margin-bottom: 8px;
    }

    @media (max-width: 1400px) {
        img {
            width: 40%;
        }
    }

    @media (max-width: 992px) {
        img {
            width: 50%;
            height: 50%;
            margin: auto;
        }

        .faq_title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 5px;
        }
    
        .faq_text {
            margin-bottom: 8px;
            font-size: 0.8rem;
            line-height: 20px;
        }

        .btn {
            font-size: 0.7rem;
            width: 130px;
            height: 30px;
        }
    }

    @media (max-width: 768px) {
        .container {
            flex-direction: column !important;
        }
    }

    @media (max-width: 576px) {
        
    }
</style>