<template>
    <div v-if="show" class="modal-shadow d-flex justify-content-center align-items-center" @click.self="closeModal">
        <div class="card d-flex justify-content-center align-items-center">
            <h3 class="title">Congratulations! Registration was successful.</h3>
            <button class="btn btn-primary" @click="closeModal">Close</button>
        </div>
    </div>
</template>
 
<script>
    export default {
        name: "ModalWindow",
        data() {
            return {
                show: false
            }
        },
        methods: {
            closeModal() {
                this.show = false
            }
        }
    }
</script>
 
<style scoped>
    .modal-shadow {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background: rgba(0, 0, 0, 0.39);
        width: 100%;
        height: 100%;
    }

    .card {
        width: 500px;
        height: 400px;
    }

    .title {
        padding: 20px;
        text-align: center;
        margin-bottom: 30px;
    }
</style>