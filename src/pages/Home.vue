<template>
    <main>
      <h1 ref="presentation" class="presentation">Andromeda Software!, Software development team.</h1>
      <img src="../assets/humans.png" alt="Human Image" id="img-presentation">
    </main>
  </template>
  
  <script>
  export default {
    name: "Home",
    mounted() {
      this.typeWrite(this.$refs.presentation);
    },
    methods: {
      typeWrite(element) {
        const textArray = element.innerHTML.split("");
        element.innerHTML = " ";
        textArray.forEach(function (letter, i) {
          setTimeout(function () {
            element.innerHTML += letter;
          }, 75 * i);
        });
  
        setTimeout(() => {
          this.$refs.presentation.classList.add('paused');
        }, 3450);
      },
    },
  };
  </script>
  
  <style scoped>
  
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  #img-presentation {
    width: 270px;
  }
  
  .presentation {
    max-width: 480px;
    text-align: center;
    margin: 20px auto;
    font-family: "Courier New", Courier, monospace;
    color: #fff;
  }
  
  .presentation:after {
    content: "|";
    margin-left: 5px;
    opacity: 1;
    animation: blink 0.7s infinite forwards;
  }
  
  .presentation.paused:after {
    display: none;
  }
  
  @keyframes blink {
    0%,
    100% {
      opacity: 1;
    }
    50% {
      opacity: 0;
    }
  }
  </style>
  