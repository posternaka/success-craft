<template>
    <div id="contact" class="wrapper">
        <div class="container">
            <h3 class="title text-center">Contact Us</h3>
            <form class="row g-3 text-left" @submit.prevent="checkForm">
                <div class="col-md-3">
                    <label for="firstname">First Name *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Firstname" 
                        id="firstname" 
                        class="form-control" 
                        :class="v$.form.firstname.$error ? 'is-invalid' : ''"
                        v-model.trim="form.firstname"
                    >
                    <div class="errors" v-if="v$.form.firstname.$dirty && !v$.form.firstname.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.firstname.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="lastname">Last name *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Lastname" 
                        id="lastname" 
                        class="form-control" 
                        :class="v$.form.lastname.$error ? 'is-invalid' : ''"
                        v-model.trim="form.lastname"
                    >
                    <div class="errors" v-if="v$.form.lastname.$dirty && !v$.form.lastname.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.lastname.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="company">Company *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Company" 
                        id="company" 
                        class="form-control" 
                        :class="v$.form.company.$error ? 'is-invalid' : ''"
                        v-model.trim="form.company"
                    >
                    <div class="errors" v-if="v$.form.company.$dirty && !v$.form.company.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.company.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="email">Email *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Email" 
                        id="email" 
                        class="form-control" 
                        :class="v$.form.email.$error ? 'is-invalid' : ''"
                        v-model.trim="form.email"
                    >
                    <div class="errors" v-if="v$.form.email.$dirty && !v$.form.email.email">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.email.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="company">Job Title *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Job Title" 
                        id="job" 
                        class="form-control" 
                        :class="v$.form.job.$error ? 'is-invalid' : ''"
                        v-model.trim="form.job"
                    >
                    <div class="errors" v-if="v$.form.job.$dirty && !v$.form.job.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.job.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="company">Country *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Country" 
                        id="country" 
                        class="form-control" 
                        :class="v$.form.country.$error ? 'is-invalid' : ''"
                        v-model.trim="form.country"
                    >
                    <div class="errors" v-if="v$.form.country.$dirty && !v$.form.country.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.country.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="company">State *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your State" 
                        id="state" 
                        class="form-control" 
                        :class="v$.form.state.$error ? 'is-invalid' : ''"
                        v-model.trim="form.state"
                    >
                    <div class="errors" v-if="v$.form.state.$dirty && !v$.form.state.required">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.state.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-md-3">
                    <label for="company">Zip Code *</label>
                    <input 
                        type="text" 
                        placeholder="Enter your Zip Code" 
                        id="zipCode" 
                        class="form-control" 
                        :class="v$.form.zipCode.$error ? 'is-invalid' : ''"
                        v-model.trim="form.zipCode"
                    >
                    <div class="errors" v-if="v$.form.zipCode.$dirty && !v$.form.zipCode.numeric">
                        <div class="error_msg">Required field</div>
                    </div>
                    <div class="errors" v-for="(error, index) of v$.form.zipCode.$errors" :key="index">
                        <div class="error_msg">{{ error.$message }}</div>
                    </div>
                </div>

                <div class="col-12 text-center page">
                    <button class="btn btn-primary">Submit</button>
                    <modal-window ref="modal"></modal-window>
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
    import { required, email, numeric} from '@vuelidate/validators';
    import ModalWindow from '@/components/modal-window.vue';

    export default {
        name: 'footer_block',
        setup () {
            return { v$: useVuelidate() }
        },
        components: {
            ModalWindow
        },
        data() {
            return {
                currentTime: 3,
                timer: null,
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
                },
                lastname: { 
                    required,
                },
                company: {
                    required, 
                },
                email: { 
                    required, 
                    email,
                },
                job: {
                    required, 
                },
                country: {
                    required, 
                },
                state: {
                    required,
                },
                zipCode: {
                    required, 
                    numeric,
                },
            },
            }
        },
        methods: {
            checkForm() {
                this.v$.form.$touch()
                if (!this.v$.form.$error) {
                    this.startTimer()
                    return this.showModal()
                }

                return false
            },
            showModal() {
                this.$refs.modal.show = true;
            },
            startTimer() {
                this.timer = setInterval(() => {
                    if (this.currentTime === 0) {
                        this.$refs.modal.show = false;
                        this.currentTime = 3;
                        clearInterval(this.timer);
                    } else {
                        --this.currentTime;
                    }             
                }, 1000)
            },
        },
    }
</script>

<style scoped>
    .page {
        position: relative;
        overflow: hidden; 
    }

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
</style>