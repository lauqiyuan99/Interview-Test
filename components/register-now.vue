<template>
  <div class="pt-5 pb-5" style="background-color: #0477b5">
    <div class="container">
      <div class="title">Register Now</div>
      <form @submit.prevent="submitForm">
        <div class="form-row row col-12 ms-0">
          <input
            class="input-text-field"
            v-model.trim="firstName"
            type="text"
            placeholder="First Name"
          />
          <input
            class="input-text-field"
            v-model.trim="lastName"
            type="text"
            placeholder="Last Name"
          />
          <input
            class="input-text-field"
            v-model.trim="email"
            type="email"
            placeholder="Email"
          />
          <input
            class="input-text-field"
            v-model.trim="password"
            type="password"
            placeholder="Password"
          />
          <input
            class="input-text-field"
            v-model.trim="confirmPassword"
            type="password"
            placeholder="Confirm Password"
          />
        </div>
        <div class="form-row d-flex col col-12">
          <select class="input-text-field col-1 me-2" v-model="country">
            <option value="">Country</option>
          </select>
          <input
            class="input-text-field col-11"
            v-model.trim="phone"
            type="text"
            placeholder="Phone"
          />
        </div>
        <div class="form-row">
          <label class="label-check-box">
            <input
              class="check-box-style mb-5"
              v-model="agreeTerms"
              type="checkbox"
            />
            I confirm that I am at least 18 years old.
          </label>
          <label class="label-check-box">
            <input color="#0477b5" v-model="receiveUpdates" type="checkbox" />
            By joining and participating in the Competition, I acknowledge and
            confirm that I have read, understood and agreed to be boured by the
            <a class="label-check-box" href="#">Term and Conditions</a> of the
            Competition
          </label>
        </div>
        <label class="label-term">
          This site is protected by reCAPTCHA and the Google
          <a class="label-check-box" href="#">Privacy Policy</a> and
          <a class="label-check-box" href="#">Term of Service</a> apply
        </label>
        <div class="form-row col-12 d-flex row mt-3 mb-3">
          <button class="register p-1" type="submit" @click="submitForm">Register Now</button>
        </div>
        <div class="form-row col-12 d-flex col">
          <div class="col-6 d-flex row me-3">
            <button class="facebook p-1" type="submit">
              Signup by Facebook
            </button>
          </div>
          <div class="col-6 d-flex row">
            <button class="google p-1" type="submit">Signup by Google</button>
          </div>
        </div>
      </form>
    </div>
    <TradeGuide />
  </div>
</template>

<script>
import { useVuelidate } from "@vuelidate/core";
import { required, email, minLength, sameAs } from "@vuelidate/validators";

export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      email: "",
      password: "",
      confirmPassword: "",
      country: "",
      phone: "",
      agreeTerms: false,
      receiveUpdates: false,
    };
  },
  validations: {
    firstName: { required },
    lastName: { required },
    email: { required, email },
    password: { required, minLength: minLength(6) },
    confirmPassword: { required, sameAsPassword: sameAs("password") },
    country: { required },
    phone: { required },
  },
  methods: {
    submitForm() {
      this.$v.$touch();
      if (!this.$v.$invalid) {
        alert("Invalid Info")
      }
    },
  },
};
</script>

<style lang="scss">
.title {
  color: #f68b1e;
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 20px;
}

::placeholder {
  color: #b9e6f9;
  opacity: 0.5;
}

.input-text-field {
  height: 40px;
  margin-bottom: 20px;
  border-top-width: 0;
  border-left-width: 0;
  border-right-width: 0;
  border-bottom-width: 1.5px;
  border-color: #b9e6f9;
  background-color: #0b7cb6;
  color: #b9e6f9;
}

.col-11 {
  width: 90.99666667% !important;
}

.label-check-box {
  color: #92bad2;
  font-size: 15px;
}

.label-term {
  color: #ced9e0;
  font-size: 15px;
}

.register {
  background-color: #999999;
  color: #d3d3d3;
  font-size: 15px;
  border: none;
  border-radius: 20px;
}

.google {
  background-color: #cf1508;
  color: #fff;
  font-size: 15px;
  border: none;
  border-radius: 20px;
}

.facebook {
  background-color: #004d8f;
  color: #e7ecf3;
  font-size: 15px;
  border: none;
  border-radius: 20px;
}
</style>
