<template>
    <div class="wrapper">
        <div class="container">
            <h1>Welcome to Test Page</h1>
            <p>Front-end developer</p>  
        </div>
    </div>
</template>

<script>
    export default {
        name: 'welcome-information',
        data() {
            return {
                message: 'Nik'
            }
        },
    };
</script>

<style scoped>
    .wrapper {
        height: 100vh;
        background: url('@/assets/header/background-header.png') ;
    }

</style>