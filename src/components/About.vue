<template>
  <v-container>
    <h2 class="headline pb-4">O stronie</h2>
    <p>
      Strona została stworzona jako praca konkursowa w konkursie <b>"Zobaczyć matematykę"</b> organizowanym przez Akademię Górniczo-Hutniczą im. Stanisława Staszica w Krakowie. Stronę wykonał <b>Filip Drozd</b>. Do poprawnego jej działanie wymagane jest połączenie z internetem.
    </p>
    <v-row align="center">
      <div class="title ml-3 pr-4">Użyte technologie: </div>
      <v-btn small depressed v-for="tech in techs" :key="tech.name" :color="tech.color" :href="tech.link" class="white--text mr-2">{{ tech.name }}</v-btn>
    </v-row>
    <p class="pt-5">
      Ikony wykonane przez <a href="https://www.flaticon.com/authors/vitaly-gorbachev" title="Vitaly Gorbachev">Vitaly Gorbachev</a> z <a href="https://www.flaticon.com/" title="Flaticon"> www.flaticon.com</a>
    </p>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      techs: [
        { name: 'html5', color: 'red', link: 'https://developer.mozilla.org/pl/docs/HTML/HTML5' },
        { name: 'css3', color: 'blue', link: 'https://developer.mozilla.org/pl/docs/Web/CSS' },
        { name: 'Vue.js', color: 'green', link: 'https://vuejs.org/' },
        { name: 'Vuetify.js', color: 'primary', link: 'https://vuetifyjs.com/en/' },
        { name: 'Chartist.js', color: 'orange', link: 'https://gionkunz.github.io/chartist-js/' }
      ]
    };
  }
}
</script>

<style>
</style>
