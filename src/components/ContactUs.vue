<!-- <template>
  <div>
    <b-form @submit.stop.prevent="onSubmit">
      <b-form-group id="example-input-group-1" label="Name" label-for="example-input-1">
        <b-form-input
          id="example-input-1"
          name="example-input-1"
          v-model="$v.form.name.$model"
          :state="validateState('name')"
          aria-describedby="input-1-live-feedback"
        ></b-form-input>

        <b-form-invalid-feedback
          id="input-1-live-feedback"
        >This is a required field and must be at least 3 characters.</b-form-invalid-feedback>
      </b-form-group>

      <b-form-group id="example-input-group-2" label="Food" label-for="example-input-2">
        <b-form-select
          id="example-input-2"
          name="example-input-2"
          v-model="$v.form.food.$model"
          :options="foods"
          :state="validateState('food')"
          aria-describedby="input-2-live-feedback"
        ></b-form-select>

        <b-form-invalid-feedback id="input-2-live-feedback">This is a required field.</b-form-invalid-feedback>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button class="ml-2" @click="resetForm()">Reset</b-button>
    </b-form>
  </div>
</template>

<style>
body {
  padding: 1rem;
}
</style>

<script>
import { validationMixin } from "vuelidate";
import { required, minLength } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],
  data() {
    return {
      foods: [
        { value: null, text: "Choose..." },
        { value: "apple", text: "Apple" },
        { value: "orange", text: "Orange" }
      ],
    }
  },
  validations: {
    form: {
      food: {
        required
      },
      name: {
        required,
        minLength: minLength(3)
      }
    }
  },
};
</script> -->


<template>
  <form @submit.prevent="onSubmit">
    <!-- First and Last Name Row -->
    <div class="row">
      <div class="col-sm-6">
        <div class="form-group">
          <label for=""> First Name:</label><input class="form-control" placeholder="Enter first name" type="text" v-model="v$.form.firstName.$model">
          <div class="pre-icon os-icon os-icon-user-male-circle"></div>
          <!-- Error Message -->
          <div class="input-errors" v-for="(error, index) of v$.form.firstName.$errors" :key="index">
            <div class="error-msg">{{ error.$message }}</div>
          </div>
        </div>
      </div>

      <div class="col-sm-6">
        <div class="form-group">
          <label for="">Last Name:</label><input class="form-control" placeholder="Enter last name" type="text" v-model="v$.form.lastName.$model">
          <!-- Error Message -->
          <div class="input-errors" v-for="(error, index) of v$.form.lastName.$errors" :key="index">
            <div class="error-msg">{{ error.$message }}</div>
          </div>
        </div>
      </div>
    </div>


    <!-- Email Row -->
    <div class="form-group">
      <label for=""> Email address</label><input class="form-control" placeholder="Enter email" type="email" v-model="v$.form.email.$model">
      <div class="pre-icon os-icon os-icon-email-2-at2"></div>
      <!-- Error Message -->
        <div class="input-errors" v-for="(error, index) of v$.form.email.$errors" :key="index">
          <div class="error-msg">{{ error.$message }}</div>
        </div>
    </div>


    <!-- Password and Confirm Password Row -->
    <div class="row">
      <div class="col-sm-6">
        <div class="form-group">
          <label for=""> Password</label><input class="form-control" placeholder="Password" type="password" v-model="v$.form.password.$model">
          <div class="pre-icon os-icon os-icon-fingerprint"></div>
          <!-- Error Message -->
          <div class="input-errors" v-for="(error, index) of v$.form.password.$errors" :key="index">
            <div class="error-msg">{{ error.$message }}</div>
          </div>
        </div>
      </div>

      <div class="col-sm-6">
        <div class="form-group">
          <label for="">Confirm Password</label><input @input="checkPassword()" class="form-control" placeholder="Confirm Password" type="password" v-model="v$.form.confirmPassword.$model">
          <!-- Error Message -->
          <div class="input-errors" v-for="(error, index) of v$.form.confirmPassword.$errors" :key="index">
            <div class="error-msg">{{ error.$message }}</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Submit Button -->
    <div class="buttons-w">
      <button class="btn btn-primary" :disabled="v$.form.$invalid" style="margin-left:120px">Signup</button>
    </div>
    
  </form>
</template>

<script>
import useVuelidate from '@vuelidate/core'
import { required, email, minLength, } from '@vuelidate/validators'


export function validName(name) {
  let validNamePattern = new RegExp("^[a-zA-Z]+(?:[-'\\s][a-zA-Z]+)*$");
  if (validNamePattern.test(name)){
    return true;
  }
  return false;
}


export default {

  setup () {
    return { v$: useVuelidate() }
  },

  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        email: '',
        password: '',
        confirmPassword: '',
      }
    }
  },

  validations() {
    return {
      form: {
        firstName: { 
          required, name_validation: {
            $validator: validName,
            $message: 'Invalid Name. Valid name only contain letters, dashes (-) and spaces'
          } 
        },
        lastName: { 
          required, name_validation: {
            $validator: validName,
            $message: 'Invalid Name. Valid name only contain letters, dashes (-) and spaces'
          } 
        },
        email: { required, email },
        password: { required, min: minLength(6) },
        confirmPassword: { required }
      },
    }
  },
}
</script>

