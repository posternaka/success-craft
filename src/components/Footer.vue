<template>
    <div class="wrapper">
        <div class="container">
            <h3 class="title text-center">Contact Us</h3>
            <form class="row g-3 text-left">
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">First Name *</label>
                    <input type="text" placeholder="Enter your First name" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Last name *</label>
                    <input type="text" placeholder="Enter your Last name" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Company *</label>
                    <input type="text" placeholder="Enter your company" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServerUsername" class="form-label">Email *</label>
                    <div class="input-group has-validation">
                    <input type="text" class="form-control" id="validationServerUsername" placeholder="Enter Your Email" aria-describedby="inputGroupPrepend3 validationServerUsernameFeedback" required>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Job Title *</label>
                    <input type="text" placeholder="Enter job title" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Country *</label>
                    <input type="text" placeholder="Enter Your Country" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">State *</label>
                    <input type="text" placeholder="Enter your State" class="form-control" id="validationServer01" required>
                </div>
                <div class="col-md-3">
                    <label for="validationServer05" class="form-label">Zip Code *</label>
                    <input type="text" class="form-control" id="validationServer05" placeholder="Enter Your Zip Code" aria-describedby="validationServer05Feedback" required>
                </div>
                <div class="col-12 text-center">
                    <button class="btn btn-primary" type="submit">Submit</button>
                </div>
            </form>
        </div>
        <div class="copyright">
            <h6>©2015-2022 Success Craft</h6>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'footer_block',
    }
</script>

<style scoped>
    .container {
        padding-top: 44px;
        padding-bottom: 59px;
    }

    .title {
        color: #000;
        margin-bottom: 44px;
    }

    .form-label {
        text-align: left;;
    }

    .btn {
        margin-top: 26px;
    }

    .copyright {
        text-align: center;
        padding: 60px 0;
        background: #3D3D3D;
        color: #fff;
    }

    h6 {
        font-size: 16px;
    }
</style>