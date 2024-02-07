<template>
    <section class="container_tec_list">
        <figure class="list_item" @click="showProjects('BOOSTSTRAP')">
            <img src="@/assets/bootstrapLogo.png" alt="bootstrap logo"  @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('CSS')">
            <img src="@/assets/cssLogo.png" alt="ccs logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('HMTL')">
            <img src="@/assets/htmlLogo.png" alt="html logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('JavaScript')">
            <img src="@/assets/jsLogo.png" alt="javaScript Logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('MONGO DB')">
            <img src="@/assets/mongoLogo.png" alt="mongo db logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('NODE')">
            <img src="@/assets/nodeLogo.png" alt="node Logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('NPM')">
            <img src="@/assets/npmLogo.png" alt="npm logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('POSTGRESQL')">
            <img src="@/assets/postgreLogo.png" alt="postgreSQL logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('REACT')">
            <img src="@/assets/reactLogo.png" alt="react logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        <figure class="list_item" @click="showProjects('VUE')">
            <img src="@/assets/vueLogo.png" alt="vue logo" @mouseover="hoverEffect" @mouseout="resetEffect">
        </figure>
        
        
    </section>
   
    
</template>

<script>
    export default {
        data() {
            return {
            showTecsDiv: false,
            selectedTech: '',
            progress: 68,
            };
        },
        methods: {
            hoverEffect(event) {
                event.target.style.transform = 'scale(2)';
            },
            resetEffect(event) {
                event.target.style.transform = 'scale(1)';
            },
            showProjects(tech) {
                this.selectedTech = tech;
                this.showTecsDiv = true;
                this.startProgressBar();
            },
            closeProjects() {
            this.showTecsDiv = false;
            },
        },
    };
</script>

<style scoped>
    /* estilos contenedor principal */
    .container_tec_list{
        width: 90%;
        margin: 20px auto;
        color: white;

        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap:10px
    }

    /* estrlos de las imágenes */
    img {
        width: 200px;
        height: 200px;
        margin: 5px;
        transition: transform 0.3s ease;
    }

    .list_item:nth-last-child(-n + 2) {
        grid-column: span 2; 
        justify-self: center;
    }

    /* estilos del div de proyectos */
    .tecs-Overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(255, 255, 255, 0); /* Fondo semi-transparente */
        backdrop-filter: blur(10px); /* Efecto glass con desenfoque */
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .projects_content {
        width: 50%;
        height: 50%;
        background-color: transparent;
        border: 1px solid gray;
        border-radius: 5px;
        padding: 20px;
        text-align: center;
        box-shadow: 0 0 3px rgba(255, 255, 255, 0.4);
    }

   

    .projects_content button {
        background-color: #3498db;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
        border-radius: 50%;
    }

</style>

