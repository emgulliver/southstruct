<template>
    <section class="section" id="contact">
      <h2 class="has-text-centered is-size-3 mb-5">{{ heading }}</h2>
      <form @submit.prevent="submitForm" class="contact-form mt-5 is-flex is-flex-direction-column is-align-items-center">
        <div class="field is-horizontal">
          <div class="field-body">
            <div class="field">
              <p class="control is-expanded">
                <input class="input" type="text" v-model="name" placeholder="Your Name" style="min-width: 350px;">
              </p>
            </div>
          </div>
        </div>
        <div class="field is-horizontal">

          <div class="field-body">
            <div class="field">
              <p class="control is-expanded">
                <input class="input" type="email" v-model="email" placeholder="Your Email" style="min-width: 350px;">
              </p>
            </div>
          </div>
        </div>
        <div class="field">
          
          <div class="control">
            <input class="input" type="text" v-model="subject" placeholder="Subject" style="min-width: 350px;">
          </div>
        </div>
        <div class="field">
        
          <div class="control">
            <textarea class="textarea" v-model="message" placeholder="Your Message" style="min-width: 350px;"></textarea>
          </div>
        </div>
        <div class="field">
          <div class="control">
            <button class="button has-background-primary has-text-white">Submit</button>
          </div>
        </div>
      </form>
    </section>
  </template>
  
  <script setup lang="ts">
  import {ref} from "vue"
  const heading = "Get Your Free Consultation";
  const name = ref("");
  const email = ref("");
  const subject = ref("");
  const message = ref("");
  
  const submitForm = () => {
  const subjectText = `${subject.value}`;
  const body = `Name: ${name.value} Message: ${message.value}`;
  const mailtoString = `mailto:drew@southstructwa.au?subject=${encodeURIComponent(subjectText)}&body=${encodeURIComponent(body)}`;
  
  window.location.href = mailtoString;
  };
  </script>
  
