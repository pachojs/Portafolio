<template>
    <div id="education-section">
      <h2>ESTUDIOS</h2>
      <div class="education-container">
        <div class="education_cards-container">
          <div class="lawyer-container">
            <button></button>
            <div class="card-Lawyer">Abogado</div>
             
          </div>
        </div>  
        <div class="developerContainer">Desarrollo web
          <button></button> 
          <div v-for="(curso, index) in cursos" :key="index" class="curso">
            {{ curso }}
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      cursos: ["Diplomado full-Stack", "Curso Backend con NODE.JS API REST CON EXPRESSJS", "Curso básico JavaScript", "Curso Frontend Developer", "Fundamentos de NODE.JS", "Curso definitivo de  HTML y CSS", "Curso practico de JavaScript"] // Arreglo con nombres de cursos
    };
  }
};
</script>

<style scoped>

.education-container{
  margin-top: 50px;
  display:flex;
  Flex-wrap: nowrap;
  justify-content: space-evenly;
}

.curso {
  /* Estilos para cada div de curso */
  margin-bottom: 10px;
  padding: 10px;
  border-radius: 5px;
}
</style>