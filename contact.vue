<template>
   <div class="contact">
     <h1>Contact Us</h1>
     <form @submit.prevent="submitForm">
       <div class="mb-3">
         <label for="name" class="form-label">Name</label>
         <input type="text" class="form-control" id="name" v-model="name" required>
       </div>
       <div class="mb-3">
         <label for="email" class="form-label">Email</label>
         <input type="email" class="form-control" id="email" v-model="email" required>
       </div>
       <div class="mb-3">
         <label for="message" class="form-label">Message</label>
         <textarea class="form-control" id="message" v-model="message" rows="3" required></textarea>
       </div>
       <button type="submit" class="btn btn-primary">Send</button>
     </form>
   </div>
 </template>
 
 <script>
 export default {
   name: 'contact',
   data() {
     return {
       name: '',
       email: '',
       message: ''
     }
   },
   methods: {
     submitForm() {
       // Handle form submission (e.g., send data to a server)
       alert(`Name: ${this.name}\nEmail: ${this.email}\nMessage: ${this.message}`);
       // Reset the form fields
       this.name = '';
       this.email = '';
       this.message = '';
     }
   }
 }
 </script>
 
 <style scoped>
 .contact {
   padding: 20px;
 }
 </style>
 