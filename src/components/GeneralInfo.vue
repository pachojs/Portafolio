<template>
    <div>
        <div class="profile">
          <span v-for="(char, index) in animatedText" :key="index" class="animacion-texto" :style="{ 'animation-delay': (index * 0.1) + 's' }">
            {{ char === ' ' ? '\u00A0' : char }}
          </span>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        text: "Soy Abogado y Desarrollador Full-stack, Aquí podrán Encontrar un poco de mi trabajo en diferentes tecnologías.",
        animatedText: [],
      };
    },
    mounted() {
      this.splitText();
    },
    methods: {
      splitText() {
        this.animatedText = this.text.split("");
      },
    },
  };
  </script>
  
  <style scoped>
  .profile {
    width: 70%;
    margin: 20px auto;
    padding: 5px;
    border: solid 1px white;
    font-size: 16px;
    overflow: hidden;
  }
  
  .animacion-texto {
    opacity: 0;
    display: inline-block;
    animation: aparecer 1s forwards;
  }
  
  @keyframes aparecer {
    to {
      opacity: 1;
    }
  }
  </style>
  