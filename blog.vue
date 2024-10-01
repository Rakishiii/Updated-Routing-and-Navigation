<template>
   <div class="blog-container">
     <h1>Meet Blackpink Members</h1>
     <div class="member" v-for="member in members" :key="member.id">
       <h2>{{ member.name }}</h2>
       <img :src="member.image" :alt="'Image of ' + member.name" class="member-image">
       <p>{{ member.description }}</p>
     </div>
     <router-link to="/">Back to Home</router-link>
   </div>
 </template>
 
 <script>
 export default {
   data() {
     return {
       members: [
         {
           id: 1,
           name: 'Jisoo',
           image: require('../assets/jisoo.jpg'),
           description: 'Jisoo is the lead vocalist of Blackpink and is known for her stunning visuals and strong stage presence.'
         },
         {
           id: 2,
           name: 'Jennie',
           image: require('../assets/jennie.jpg'), 
           description: 'Jennie is the main rapper and is recognized for her unique style and charisma.'
         },
         {
           id: 3,
           name: 'Rosé',
           image: require('../assets/rose.jpg'), 
           description: 'Rosé is the main vocalist and is loved for her exceptional voice and emotional performances.'
         },
         {
           id: 4,
           name: 'Lisa',
           image: require('../assets/lisa.jpg'), 
           description: 'Lisa is the main dancer and is famous for her powerful dance moves and magnetic personality.'
         }
       ]
     };
   }
 }
 </script>
 
 <style scoped>
 .blog-container {
   padding: 20px;
   text-align: center;
 }
 .member {
   margin-bottom: 40px; 
 }
 .member-image {
   width: 200px; 
   height: auto;
   border-radius: 10px; 
 }
 </style>
 