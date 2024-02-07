<<template>
    <div class="starry-background">
      <div v-for="star in stars" :key="star.id" class="star" :style="star.style"></div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        stars: [],
      };
    },
    mounted() {
      this.generateStars();
    },
    methods: {
      generateStars() {
        const starCount = 50;
        for (let i = 0; i < starCount; i++) {
          this.stars.push({
            id: i,
            style: {
              left: `${Math.random() * 100}%`,
              animationDuration: `${Math.random() * 2 + 1}s`,
              animationDelay: `${Math.random()}s`,
            },
          });
        }
      },
    },
  };
  </script>
  
  <style>
  .starry-background {
    position: fixed;
    width: 100%;
    height: 100%;
    background: transparent;
    z-index: -1;
  }
  
  .star {
    position: absolute;
    width: 2px;
    height: 2px;
    background-color: white;
    border-radius: 50%;
    opacity: 0.8;
    animation: moveStar 3s linear infinite;
  }
  
  @keyframes moveStar {
    0% {
      transform: translateY(100vh);
    }
    100% {
      transform: translateY(-100vh);
    }
  }
  </style>