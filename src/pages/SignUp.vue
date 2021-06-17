
<template>
  <div class="flex flex-col min-h-screen overflow-hidden">
    <!-- Site header -->
    <Header />

    <!-- Page content -->
    <main class="flex-grow">
      <!-- Page illustration -->
      <div
        class="relative max-w-6xl mx-auto h-0 pointer-events-none"
        aria-hidden="true"
      >
        <PageIllustration />
      </div>

      <section class="relative">
        <div class="max-w-6xl mx-auto px-4 sm:px-6">
          <div class="pt-32 pb-12 md:pt-40 md:pb-20">
            <!-- Page header -->
            <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
              <h1 class="h1">Get Early Access</h1>
            </div>

            <!-- Form -->
            <div class="max-w-sm mx-auto">
              <form>
                <div class="flex flex-wrap -mx-3"></div>
              </form>
              <div class="flex items-center my-6">
                <div
                  class="border-t border-gray-700 border-dotted flex-grow mr-3"
                  aria-hidden="true"
                ></div>
                <div class="text-gray-800">Register with your email</div>
                <div
                  class="border-t border-gray-700 border-dotted flex-grow ml-3"
                  aria-hidden="true"
                ></div>
              </div>
              <form>
                <div class="flex flex-wrap -mx-3 mb-4">
                  <div class="w-full px-3">
                    <label
                      class="block text-gray-600 text-sm font-medium mb-1"
                      for="full-name"
                      >Full Name <span class="text-red-600">*</span></label
                    >
                    <input
                      v-model="full_name"
                      type="text"
                      class="form-input w-full text-gray-600"
                      placeholder="First and last name"
                      required
                    />
                  </div>
                </div>
                <div class="flex flex-wrap -mx-3 mb-4">
                  <div class="w-full px-3">
                    <label
                      class="block text-gray-600 text-sm font-medium mb-1"
                      for="company-name"
                      >Company Name <span class="text-red-600">*</span></label
                    >
                    <input
                      v-model="company"
                      type="text"
                      class="form-input w-full text-gray-600"
                      placeholder="Your company"
                      required
                    />
                  </div>
                </div>
                <div class="flex flex-wrap -mx-3 mb-4">
                  <div class="w-full px-3">
                    <label
                      class="block text-gray-600 text-sm font-medium mb-1"
                      for="email"
                      >Work Email <span class="text-red-600">*</span></label
                    >
                    <input
                      v-model="email"
                      type="email"
                      class="form-input w-full text-gray-600"
                      placeholder="you@yourcompany.com"
                      required
                    />
                  </div>
                </div>

                <div class="text-sm text-gray-500 text-center">
                  I agree to be contacted by Foresight
                  <a
                    class="
                      underline
                      text-gray-800
                      hover:text-gray-200
                      hover:no-underline
                      transition
                      duration-150
                      ease-in-out
                    "
                    href="#0"
                    >Privacy Policy</a
                  >.
                </div>
                <div class="flex flex-wrap -mx-3 mt-6">
                  <div class="w-full px-3">
                    <button
                      type="button"
                      v-on:click="emailFunction"
                      class="
                        btn
                        text-white
                        bg-purple-600
                        hover:bg-purple-700
                        w-full
                      "
                    >
                      Sign up
                    </button>
                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Site footer -->
    <Footer />
  </div>
</template>

<script>
import Header from "./../partials/Header.vue";
import PageIllustration from "../partials/PageIllustration.vue";
import Footer from "./../partials/Footer.vue";
import axios from 'axios' 
 
export default {
  name: "SignUp",
   data() {
    return {
      full_name: "",
      company: "",
      email:"",
    }
  },
  
  methods: {
    emailFunction: function () {
      /*
      var axios = require('axios')
      var data = JSON.stringify({
        "name": this.full_name,
        "company": this.company,
        "email": this.email,
      });
      var config = {
        method: 'post',
        url: 'https://brnxiq1j5j.execute-api.us-east-1.amazonaws.com/staging/',
        headers: {
            'Content-Type':'application/json'
         },
         data: data,
      }
      axios(config).then(function(response) {
        console.log(JSON.stringify(response.data));
      }).catch(function (error) {
        console.log(error);
      });
      */
      // console.log("Pre Axios has been reached")
      axios.post(
        "https://brnxiq1j5j.execute-api.us-east-1.amazonaws.com/staging/",
        { 
          name: this.full_name,
          company: this.company,
          email: this.email,
        }, { headers: {
            'Content-Type':'application/json'
         }
         }).then((response) => {
            console.log("this part has been reached")
            console.log(response);
            if (response.status === 200) {
              alert(
                "Thank you for your interest, " +
                  this.full_name +
                  ". \n Our team will be in touch with you shortly!"
              );
            } else {
              alert(
                "There was an unexpected error. Please contact info@gainforesight.co"
              );
            }
          })
          .catch((error) => {
            console.log(error);
          }) 
    }, 
  },
  components: {
    Header,
    PageIllustration,
    Footer,
  },
};
</script>
