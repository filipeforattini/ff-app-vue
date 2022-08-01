<script setup>
const {
  VITE_MY_VAR = 'default',
  VITE_A = 'default',
  VITE_B = 'default',
  VITE_C = 'default',
} = import.meta.env

</script>

<template>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <p>
        <code>MY_VAR</code> = {{VITE_MY_VAR}}
      </p>
      <p>A={{VITE_A || ''}} | B={{VITE_B || ''}} | C={{VITE_C || ''}}</p>
    </div>

</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
