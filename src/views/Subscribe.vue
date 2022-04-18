<template>
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary shadow border-0">
        <!-- <div class="card-header bg-transparent pb-5">
          <div class="text-muted text-center mt-2 mb-3">
            <small>Sign in with</small>
          </div>
          <div class="btn-wrapper text-center">
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="img/icons/common/github.svg"
              /></span>
              <span class="btn-inner--text">Github</span>
            </a>
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="img/icons/common/google.svg"
              /></span>
              <span class="btn-inner--text">Google</span>
            </a>
          </div>
        </div> -->
        <div class="card-body px-lg-5 py-lg-5">
          <!-- <div class="text-center text-muted mb-4">
            <small>Or sign in with credentials</small>
          </div> -->
          <form role="form" id="email_form" ref="email_form" action="http://teebr.com">

            <base-input
              formClasses="input-group-alternative mb-3"
              placeholder="Full name"
              addon-left-icon="ni ni-lock-circle-open"
              v-model="model.name"
            >
            </base-input>

            <base-input
              formClasses="input-group-alternative mb-3"
              placeholder="Email address"
              addon-left-icon="ni ni-email-83"
              v-model="model.email"
            >
            </base-input>

            <!-- <base-checkbox class="custom-control-alternative">
              <span class="text-muted">Remember me</span>
            </base-checkbox> -->
            <div class="text-center">
              <base-button type="primary" v-on:click="send" class="my-4">Get promo code</base-button>
              <base-button type="secondary" class="my-4">Skip</base-button>
            </div>
          </form>
        </div>
      </div>
      <!-- <div class="row mt-3">
        <div class="col-6">
          <a href="#" class="text-light"><small>Forgot password?</small></a>
        </div>
        <div class="col-6 text-right">
          <router-link to="/register" class="text-light"
            ><small>Create new account</small></router-link
          >
        </div>
      </div> -->
    </div>
  </div>
</template>
<script>

export default {
  name: "Subscribe",
  methods : {
    send : function () {
      // console.log(this.$refs['email_form'].id)
      this.$refs['email_form'].submit()
      // document.getElementById('email_form').submit()
    }
  },
  data() {
    return {
      model: {
        email: "",
        name: "",
      },
    };
  }
};
</script>
<style></style>
