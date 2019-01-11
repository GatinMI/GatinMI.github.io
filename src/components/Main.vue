<template>
  <section class="container">
    <div>
      <h1 class="title">
        {{ $t('fullname') }}
      </h1>
      <ul class="program-languages">
        <li class="program-languages_language" v-for="language in languages"><span class="program-languages_language-title">{{language.title}}</span>
          <ul class="program-languages_language-technologies">
            <li class="program-languages_language-technology" v-for="technology in language.technologies">{{technology}}</li>
          </ul>
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
  export default {
    data() {
      return {
        languages: [
          {
            title: 'Java',
            technologies: ['Spring', 'Hibernate']
          },
          {
            title: 'Python',
            technologies: ['Flask', 'Django']
          },
          {
            title: 'JavaScript/html/css',
            technologies: ['Node.js', 'Express.js', 'Jquery', 'Vue.js', 'Bootstrap', 'Nuxt'],
          },
          {
            title: 'LAMP',
            technologies: ['Wordpress'],
          },
          {
            title: 'Databases',
            technologies: ['MySQL', 'PostgreSQL', 'Oracle', 'MongoDB'],
          }
        ]
      }
    }
  }
</script>
<style lang="scss">
  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
    display: block;
    font-weight: 300;
    font-size: 8rem;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 5rem;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 1.5rem;
  }

  .program-languages {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    font-size: 2rem;
    &_language {

      margin: 0.5rem;
    }
    &_language-title {
      background-color: rgba(203, 209, 211, .3);
      color: #666;
      padding: .5rem 1rem;
      line-height: 3.5rem;
      border-radius: .4rem;
    }
    &_language-technologies {
      font-size: 1.5rem;
      margin: auto;
      display: flex;
      max-width: 15rem;
      justify-content: center;
      flex-wrap: wrap;
    }
    &_language-technology {
      margin: 0.5rem 1rem;
    }
  }
</style>
