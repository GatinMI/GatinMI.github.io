<template>
  <div>
    <LangChooser class="lang-chooser"></LangChooser>
    <div>
      <Main></Main>
    </div>
  </div>

</template>

<script>

  import Main from '~/components/Main.vue'
  import LangChooser from '~/components/LangChooser.vue'

  export default {
    components: {
      Main,
      LangChooser
    }
  }
</script>

<style lang="scss">
  .container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    &:nth-child(even) {
      background: #d6d6d6;
    }
  }

  .links {
    padding-top: 1.5rem;
  }
  .lang-chooser {
    position: fixed;
    top: 1rem;
    right: 1rem;
  }

</style>

