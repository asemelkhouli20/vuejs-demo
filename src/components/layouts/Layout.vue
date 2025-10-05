<script setup>
</script>

<template>
      <header></header>
      <main class="container">
            <slot />
      </main>

      <footer>
            <small>Created By Asem, by Tutorial from </small>
            <a href="https://github.com/jamezmca" target="_blank">
                  <img src="https://github.com/jamezmca.png" alt="jamezmca" />
                  <span class="text-gradient">jamezmca</span>
                  <i class="fa-brands fa-github"></i>
            </a>
      </footer>
</template>

<style scoped>
header,
footer,
main {
      padding: 1rem;
      width: 100%;
      max-width: 700px;
      margin: 0 auto;
}
main {
      flex: 1;
}
footer {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 3rem 0;
      padding-bottom: 3rem;
      gap: 0.5rem;
}
footer a {
     display: flex;
     align-items: center;
     gap: 0.5rem;
     padding: 0.3rem;
     padding-right: 0.5rem;
     background: var(--background-muted);
     border-radius: 4rem;
     border: 1px solid transparent;
     transition: 200ms;
     text-decoration: none;
}
footer a img {
      max-width: 30px;
      aspect-ratio: 1/1;
      border-radius: 100%;
}
footer a:hover {
      border-color: var(--color-link);
}

</style>
