<template>
  <div>
    Example of Transition
  </div>
  <hr/>

  <h2>fade Example</h2>
  <button @click="show = !show">Toggle Slide + Fade</button>
  <Transition name="slide-fade">
    <p v-if="show">hello</p>
  </Transition>
  <hr/>

  <h2> Bounce Example</h2>
  <button @click="bouncey = !bouncey">Toggle</button>
  <Transition name="bounce">
    <p v-if="bouncey" style="margin-top: 20px; text-align: center;">
      Hello here is some bouncy text!
    </p>
  </Transition>
  <hr/>

  <h2>Animate Example</h2>
  <button @click="animate = !animate">Toggle</button>
  <Transition
    name="custom-classes"
    enter-active-class="animate__animated animate__tada"
    leave-active-class="animate__animated animate__bounceOutRight"
  >
    <p v-if="animate">hello</p>
  </Transition>
  <hr/>


</template>

<script>
  export default {
    name:'App',
    data() {
      return {
        show: true,
        bouncey: true,
        animate: true,
      }
    }

  }
</script>

<style scoped>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

hr {
  border: 2px solid #035891;
}

/*
  Enter and leave animations can use different
  durations and timing functions.
*/
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}

/* bounce css */
.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.25);
  }
  100% {
    transform: scale(1);
  }
}

/* import animate css file */
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css";

</style>