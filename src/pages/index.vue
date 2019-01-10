<template>
  <div>
    <Main></Main>
  </div>

</template>

<script>

import Main from '~/components/Main.vue'

export default {
    components : {
        Main,
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

</style>

