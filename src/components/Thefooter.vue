<template>
    <div>
        <footer>
            <h1>Contacto y redes sociales</h1>
            <div class="container_social_media">
                <a href="#" aria-label="Facebook" class="social-link"><img src="@/assets/facebook (1).png" alt="Facebook"></a>
                <a href="#" aria-label="GitHub" class="social-link"><img src="@/assets/github.png" alt="GitHub"></a>
                <a href="#" aria-label="Instagram" class="social-link"><img src="@/assets/instagram (1).png" alt="Instagram"></a>
                <a href="#" aria-label="LinkedIn" class="social-link"><img src="@/assets/linkedin.png" alt="LinkedIn"></a>
            </div>
        </footer>
    </div>
</template>

<style scoped>

footer {
    width: 100%;
    height: 35vh;
    background: linear-gradient(to top, #000, #1d1e2f);
    color: white;
    padding: 20px;
    text-align: center;
    font-family: 'Times New Roman', Times, serif;
    }

.container_social_media {
    margin-top: 20px;
    
}

.social-link {
  display: inline-block;
  margin: 10px;
  overflow: hidden; /* Asegura que la transición no se vea afectada por el contenido */
  transition: transform 0.3s ease;
}

.social-link:hover {
  transform: scale(1.2);
}

.social-link img {
  width: 50px;
  filter: invert();
}

</style>