<template>
    <div class="wrapper">
        <div class="container">
            <h3 class="title text-center">Contact Us</h3>
            <form class="row g-3 text-left">
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">First Name *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your First name" 
                        class="form-control" 
                        id="validationServer01" 
                        v-model.trim="v$.form.firstname.$model" 
                        :class="{'is-invalid':!v$.form.firstname.$errors, 'is-valid':!v$.form.firstname.$invalid}" 
                    >
                    <div class="errors" v-for="(error, index) of v$.form.firstname.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Last name *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Last name" 
                        class="form-control" 
                        id="validationServer01" 
                        v-model.trim="v$.form.lastname.$model" 
                        :class="{'is-invalid':!v$.form.lastname.$errors, 'is-valid':!v$.form.lastname.$invalid}" 
    
                    >
                    <div class="errors" v-for="(error, index) of v$.form.lastname.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Company *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your company" 
                        class="form-control" 
                        id="validationServer01" 
                        v-model.trim="v$.form.company.$model" 
                        :class="{'is-invalid':!v$.form.company.$errors, 'is-valid':!v$.form.company.$invalid}"
                    >
                    <div class="errors" v-for="(error, index) of v$.form.company.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServerUsername" class="form-label">Email *</label>
                    <div class="input-group has-validation">
                    <input 
                        type="text" 
                        class="form-control" 
                        id="validationServerUsername" 
                        placeholder="Enter Your Email" 
                        aria-describedby="inputGroupPrepend3 validationServerUsernameFeedback" 
                        v-model.trim="v$.form.email.$model" 
                        :class="{'is-invalid':!v$.form.email.$errors, 'is-valid':!v$.form.email.$invalid}"
                    >
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.email.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Job Title *</label>
                    <input 
                        type="text" 
                        placeholder="Enter job title" 
                        class="form-control" id="validationServer01" 
                        v-model.trim="v$.form.job.$model"
                        :class="{'is-invalid':!v$.form.job.$errors, 'is-valid':!v$.form.job.$invalid}"
                    >
                    <div class="errors" v-for="(error, index) of v$.form.job.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">Country *</label>
                    <input 
                        type="text" 
                        placeholder="Enter Your Country" 
                        class="form-control" 
                        id="validationServer01" 
                        v-model.trim="v$.form.country.$model" 
                        :class="{'is-invalid':!v$.form.country.$errors, 'is-valid':!v$.form.country.$invalid}"
                    >
                    <div class="errors" v-for="(error, index) of v$.form.country.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer01" class="form-label">State *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your State" 
                        class="form-control" 
                        id="validationServer01" 
                        v-model.trim="v$.form.state.$model" 
                        :class="{'is-invalid':!v$.form.state.$errors, 'is-valid':!v$.form.state.$invalid}"
                    >
                    <div class="errors" v-for="(error, index) of v$.form.state.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>
                <div class="col-md-3">
                    <label for="validationServer05" class="form-label">Zip Code *</label>
                    <input 
                        type="text" 
                        class="form-control" 
                        id="validationServer05" 
                        placeholder="Enter Your Zip Code" 
                        aria-describedby="validationServer05Feedback" 
                        v-model.trim="v$.form.zipCode.$model" 
                        :class="{'is-invalid':!v$.form.zipCode.$errors, 'is-valid':!v$.form.zipCode.$invalid}"
                    >
                    <div class="errors" v-for="(error, index) of v$.form.zipCode.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-12 text-center">
                    <button type="submit" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal" >
                        Submit
                    </button>
                </div>

                <div v-if="showModal" @close="showModal = false">Hello</div>

                <button class="btn" @click="showModal=true">Show</button>
                <div v-if="showModal" @close="showModal = false" name="Umesh">
                    <p>dsfkdskf</p>
                </div>
                
            </form>
        </div>
        <div class="copyright">
            <h6>©2015-2022 Success Craft</h6>
        </div>
    </div>
</template>

<script>
    import useVuelidate from '@vuelidate/core';
    import { required, email, minLength, maxLength, numeric} from '@vuelidate/validators';


    export function validText(name) {
        let validNamePattern = new RegExp("^[a-zA-Z]+(?:[-'\\s][a-zA-Z]+)*$");
        if (validNamePattern.test(name)) {
            return true;
        }
        return false;
    }

    export default {
        name: 'footer_block',
        setup () {
            return { v$: useVuelidate() }
        },
        data() {
            return {
                showModal: false,
                form: {
                    firstname: '',
                    lastname: '',
                    company: '',
                    email: '',
                    job: '',
                    country: '',
                    state: '',
                    zipCode: '',
                }
            }
        },
        validations() {
            return {
            form: {
                firstname: { 
                    required, 
                    name_validation: {
                        $validator: validText,
                        $message: 'Only letters'
                    },
                    min: minLength(3),
                    max: maxLength(20),
                },
                lastname: { 
                    required, 
                    name_validation: {
                        $validator: validText,
                        $message: 'Only letters'
                    },
                    min: minLength(3),
                    max: maxLength(20),
                },
                company: {
                    required, 
                    min: minLength(3),
                    max: maxLength(20),
                },
                email: { 
                    required, 
                    email,
                },
                job: {
                    required, 
                    min: minLength(3),
                    max: maxLength(20),
                },
                country: {
                    required, 
                    min: minLength(3),
                    max: maxLength(20),
                },
                state: {
                    required,
                    min: minLength(3),
                    max: maxLength(20),
                },
                zipCode: {
                    required,
                    numeric,
                },
            },
            }
        },
    }
</script>

<style scoped>
    .container {
        padding-bottom: 59px;
    }

    .title {
        color: #000;
        margin: 44px 0;
    }

    .form-label {
        text-align: left;
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

    .error_msg {
        font-size: 12px;
        color: red;
    }

    @media (max-width: 992px) {
        .title {
            margin: 24px 0;
        }

        .form-label {
            font-size: 0.8rem;
        }

        input::placeholder {
            font-size: 0.8rem;
        }
    }

    @media (max-width: 768px) {
        
    }
</style>