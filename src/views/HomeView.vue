<template>
  <div class="home">
    <StarryBackground></StarryBackground>
    <div>
      <img src="../assets/pngegg.png" alt="logo inicial" class="first_image">
      <h1 id="MyName">FRANCISCO BEDOYA</h1>
    </div>
    <GeneralInfoVue></GeneralInfoVue>
    <h2 id="tecnologies">Tecnologías</h2>
    <tecList></tecList>
  </div>
</template>

<script>
// @ is an alias to /src

import StarryBackground from '@/components/StarryBackground.vue';
import GeneralInfoVue from '../components/GeneralInfo.vue';
import tecList from '@/components/tecList.vue';

export default {
  name: 'HomeView',
  components: {
   StarryBackground,
   GeneralInfoVue,
   tecList
}
}
</script>

<style scoped>

.first_image{
  margin-top: 30px;
  width: 25%;
  filter: invert() opacity(70%);
}

#MyName{
  margin-top: 20px;
  margin-bottom: 20px;
  font-family: 'Times New Roman', Times, serif;
  font-size: 2.5rem;
}
#tecnologies{
  font-family: 'Times New Roman', Times, serif;
  font-size: 2.5rem;
}

</style>