<template>
  <div class="AboutMeView">
    <starry-background></starry-background>
    <h1>FRANCISCO JAVIER BEDOYA VELEZ</h1>
    <div class="general-info-container">
      <img src="../assets/Imagen de WhatsApp 2023-11-03 a las 15.15.27_da59f8bd.jpg" alt="personal-picture">
      <p> Abogado con 10 años de experiencia legal, experto en resolución de conflictos,
          análisis crítico e investigación. Apasionado por la programación, el desarrollo web y la ciberseguridad, certificado en JavaScript y versado en frameworks como Vue.js, React.js, Node y Express. Destreza en bases de datosPostgreSQL y Mongo DB. Mi transición demuestra adaptabilidad yperseverancia. Busco aplicar mis habilidades analíticas, investigativasy de resolución de problemas en el desarrollo de software, aportandouna perspectiva única y sólida ética de trabajo. Listo para enfrentarnuevos retos y crecer como desarrollador de software.
      </p>
    </div>
    <proficiencyCards></proficiencyCards>
    <educationSection></educationSection>

  </div>
  
</template>

<script>

import StarryBackground from '@/components/StarryBackground.vue';
import ProficiencyCards from '@/components/proficiencyCards.vue';
import educationSection from '@/components/educationSection.vue';

export default {
  name: 'AboutView',
  components: {
    StarryBackground,
    ProficiencyCards,
    educationSection,
}
}
</script>

<style scoped>

.general-info-container{
  display: flex;
  margin: 50px;
}

.general-info-container img {
  width: 30rem;
  border-radius: 50%;
  border: solid 1px white;
  box-shadow: 0 8px 32px rgba(31, 222, 130, 0.46);
}

.general-info-container p {
  text-align: justify;
  margin: 30px;
  padding: 10px;
}

</style>
