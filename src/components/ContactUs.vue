<template>
    <div class="card">
        <h3 class="card-header text-center">Register Area</h3>
        <div class="card-body">
            <form>
                <div class="form-row">
                    <div class="form-group col-md-6">
                        <label>First Name</label>
                        <input type="text" class="form-control" v-model="firstname" :error-messages="firstnameErrors">
                    </div>
                    <!-- <div class="form-group col-md-6">
                        <label>First Name</label>
                        <input type="text" class="form-control" v-model.trim="$v.firstname.$model" :class="{'is-invalid' :$v.firstname.$error, 'is-valid' :!$v.firstname.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <p v-if="!$v.firstname.required">First name is required.</p>
                        </div>
                    </div> -->
                    <!-- <div class="form-group col-md-6">
                        <label>Last Name</label>
                        <input type="text" class="form-control" v-model.trim="$v.lastname.$model" :class="{'is-invalid':$v.lastname.$error, 'is-valid':!$v.lastname.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.lastname.required">First name is required.</span>
                            <span v-if="!$v.lastname.minLength">First name is required {{$v.lastname.$params.minLength.min}}.</span>
                            <span v-if="!$v.lastname.maxLength">First name is required {{$v.lastname.$params.maxLength.max}}.</span>
                        </div>
                    </div>
                    <div class="form-group col-md-6">
                        <label>Company</label>
                        <input type="text" class="form-control" v-model.trim="$v.company.$model" :class="{'is-invalid':$v.company.$error, 'is-valid':!$v.company.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.company.required">First name is required.</span>
                            <span v-if="!$v.company.minLength">First name is required {{$v.company.$params.minLength.min}}.</span>
                            <span v-if="!$v.company.maxLength">First name is required {{$v.company.$params.maxLength.max}}.</span>
                        </div>
                    </div>
                    <div class="form-group col-md-6">
                        <label>Email</label>
                        <input type="text" class="form-control" v-model.trim="$v.email.$model" :class="{'is-invalid':$v.email.$error, 'is-valid':!$v.email.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.email.required">First name is required.</span>
                            <span v-if="!$v.email.minLength">First name is required {{$v.email.$params.minLength.min}}.</span>
                            <span v-if="!$v.email.maxLength">First name is required {{$v.email.$params.maxLength.max}}.</span>
                        </div>
                    </div>
                    <div class="form-group col-md-6">
                        <label>Job Title</label>
                        <input type="text" class="form-control" v-model.trim="$v.jobTitle.$model" :class="{'is-invalid':$v.jobTitle.$error, 'is-valid':!$v.jobTitle.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.jobTitle.required">First name is required.</span>
                            <span v-if="!$v.jobTitle.minLength">First name is required {{$v.jobTitle.$params.minLength.min}}.</span>
                            <span v-if="!$v.jobTitle.maxLength">First name is required {{$v.jobTitle.$params.maxLength.max}}.</span>
                        </div>
                    </div>
                    <div class="form-group col-md-6">
                        <label>State</label>
                        <input type="text" class="form-control" v-model.trim="$v.state.$model" :class="{'is-invalid':$v.state.$error, 'is-valid':!$v.state.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.state.required">First name is required.</span>
                            <span v-if="!$v.state.minLength">First name is required {{$v.state.$params.minLength.min}}.</span>
                            <span v-if="!$v.state.maxLength">First name is required {{$v.state.$params.maxLength.max}}.</span>
                        </div>
                    </div>
                    <div class="form-group col-md-6">
                        <label>Zip Code</label>
                        <input type="text" class="form-control" v-model.trim="$v.zipCode.$model" :class="{'is-invalid':$v.zipCode.$error, 'is-valid':!$v.zipCode.$invalid }">
                        <div class="valid-feedback">Your right!</div>
                        <div class="invalid-feedback">
                            <span v-if="!$v.zipCode.required">First name is required.</span>
                            <span v-if="!$v.zipCode.numeric">First name is required.</span>
                        </div>
                    </div> -->
                </div>
            </form>
        </div>
    </div>
</template>


<script>
    import useValidate from '@vuelidate/core'
    import { validationMixin } from 'vuelidate';
    import { required } from 'vuelidate/lib/validators';

    export default {
        name: 'form_vue',
        mixins: [validationMixin, ],
        data() {
            return {
                v$: useValidate(),
                firstname: '',
                // lastname: '',
                // company: '',
                // email: '',
                // jobTitle: '' ,
                // country: '',
                // state: '',
                // zipCode: 0,
            }
        },
        validations: {
            firstname: {
                required,
            },
            // lastname: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // company: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // email: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // jobTitle: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // country: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // state: {
            //     required,
            //     minLength: minLength(3),
            //     maxLength: maxLength(20),
            // },
            // zipCode: {
            //     required,
            //     numeric,
            // },
        },
        computed: {
            firstnameErrors() {
                const errors = [];
                if(!this.$v.firstname.required) errors.push('Обязательно для заполнения');
                return errors;
            }
        }
    }
</script>


<style>

</style>