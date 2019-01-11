<template>
  <ul class="langs">
    <li v-for="(lang, i) in langs" :key="`Lang${i}`" :value="lang" @click="$i18n.locale=lang" class="lang" :class="{'active-lang': $i18n.locale==lang}">{{ lang }}</li>
  </ul>
</template>
<script>
 export default {
     data() {
         return {
             langs : ['ru', 'en']
         }
     }
 }
</script>
<style lang="scss" scoped>
  .langs {
    display: flex;
  }
  .lang{
    cursor: pointer;
    padding: .5rem 1rem;
    $lang-b-r: 5px;
    &:first-child{
      border-radius: $lang-b-r 0 0 $lang-b-r;
    }
    &:last-child{
      border-radius: 0 $lang-b-r $lang-b-r 0;
    }
  }

  .active-lang {
    background: rgba(42, 193, 78, 0.61);
  }
</style>
