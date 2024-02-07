<template>
    <div class="proficiency-container">
      <h2 class="mb-5">COMPETENCIAS</h2>
      <b-row>
        <b-col md="4" v-for="competencia in competencias" :key="competencia">
          <b-card
            class="competencia-card"
            @click="mostrarDetalles(competencia)"
            @mouseover="startRotation"
            @mouseout="resetRotation"
          >
            <h4>{{ competencia }}</h4>
          </b-card>
        </b-col>
      </b-row>
      <!-- ... -->
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        competencias: [
          "Resolución de problemas",
          "Pensamiento analítico",
          "Orientación al logro",
          "Trabajo en Equipo",
          "Comunicación asertiva",
          "Capacidad de adaptación",
          "Autogestión",
          "Proactivo",
          "Innovador"
        ],
        competenciaSeleccionada: null
      };
    },
    methods: {
      mostrarDetalles(competencia) {
        this.competenciaSeleccionada = competencia;
      },
      resetearSeleccion() {
        this.competenciaSeleccionada = null;
      },
      startRotation(event) {
        event.currentTarget.style.transform = 'rotateY(360deg)';
      },
      resetRotation(event) {
        event.currentTarget.style.transform = 'rotateY(0deg)';
      }
    }
  };
  </script>
  
  
  <style scoped>
  .proficiency-container {
    margin: 100px;
  }

  .competencia-card {
    margin-bottom: 20px;
    transition: transform 1.5s ease;
  }

  .competencia-card:hover {
  transform: rotateY(180deg);
  }

  </style>
  