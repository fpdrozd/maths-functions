<template>
  <v-container>
    <h2 class="headline pb-4">Czym jest funkcja?</h2>

    <p>
      Funkcja to bardzo ważne i często spotykane pojęcie w matematyce. Jednak czym ona jest? Jakie wyróżniamy rodzaje funkcji? Jakie ma ona zastosowania? Niniejsza strona została stworzona, aby odpowiedzieć na te pytania. Zacznijmy jednak od definicji podręcznikowej:
    </p>
    <v-alert border="left" colored-border color="red">
      <div class="title">
        Definicja
      </div>
      <div>
        Funkcją ze zbioru <b>X</b> w zbiór <b>Y</b> nazywamy przyporządkowanie, w którym każdemu elementowi <b>x &isin; X</b> odpowiada dokładnie jeden element <b>y &isin; Y</b>. Zbiór <b>X</b> nazywamy <b>dziedziną</b> funkcji, a jego elementy <b>argumentami</b>.
      </div>
    </v-alert>
    <p>
      Innymi słowy funkcją nazywamy przyporządkowanie każdemu elementowi pewnego zbioru dokładnie jednego elementu drugiego zbioru. Chyba najpopularniejszym przykładem zastosowania funkcji podawanym w szkole jest ten w którym to każdemu uczniowi przyporządkowywany jest unikatowy numer w dzienniku. Tak określone przypożądkowanie bedzie funkcją, ponieważ jednemu uczniowi przypisany jest jeden i <b>tylko jeden numer</b>. Przykładowo: gdybyśmy chcieli danemu uczniowi przypożądkować jego oceny z matematyki, to nie moglibyśmy tego nazwać funkcją ponieważ jedna osoba zazwyczaj posiada kilka ocen.
    </p>
    <v-alert border="left" colored-border color="red">
      <div class="title">
        Mejsce zerowe
      </div>
      <div>
        Miejscem zerowym funkcji <b>y = f(x)</b> nazywamy taki argument <b>x</b>, dla którego <b>f(x) = 0</b>.
      </div>
    </v-alert>
    <p>
      Popularnym sposobem przedstawienia funkcji jest tabelka, w której ładnie widać jakiemu argumentowi funkji przypisana jest jaka wartość. Przykład z uczniami i ich ocenami wyglądałby następująco:
    </p>
    <v-simple-table class="mb-6" dense>
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Dziedzina (Imię ucznia)</th>
            <th class="text-left">Wartość (Numer w dzienniku)</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="student in students" :key="student.name">
            <td>{{ student.name }}</td>
            <td>{{ student.v }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
    <p>
      Innym, dla niektórych przyjemniejszym dla oka sposobem przedstawienia funkcji jest wykres, gdzie oś <b>x</b> odpowiada zbiorowi <b>X</b>, a oś <b>y</b> zbiorowi <b>Y</b>.
    </p>
    <div class="ct-chart-1"></div>
    <v-alert class="mt-2" border="left" colored-border color="red">
      <div>
        Aby określić funkcję, należy podać zbiory <b>X</b> i <b>Y</b> oraz regułę, według której argumentom ze zbioru <b>X</b> przyporządkowujemy elementy ze zbioru <b>Y</b>, zwane <b>wartościami funkcji</b>.
      </div><br>
      <div>
        Zwykle funkcje oznaczamy małymi literami, na przykład: f, g, h
      </div>
    </v-alert>
    <p>
      To właśnie od tej "reguły" zależy jakie nasza funkcja będzie przyjmowała wartości. Na jej podstawie wyróżniamy wiele rodzajów funkcji:
    </p>
    <v-row class="py-10" justify="center">
      <v-btn v-for="section in nav" :key="section.id" class="mx-2 mb-2" color="red" outlined @click="$vuetify.goTo(section.id)">
        {{ section.title }}
      </v-btn>
    </v-row>
    <v-divider></v-divider>
  </v-container>
</template>

<script>
import Chartist from 'chartist'

export default {
  data: () => ({
    students: [
      { name: 'Janek', v: 4 },
      { name: 'Ania', v: 1 },
      { name: 'Paweł', v: 3 },
      { name: 'Damian', v: 6 },
      { name: 'Natalia', v: 5 },
      { name: 'Jakub', v: 9 },
      { name: 'Weronika', v: 7 },
    ],
    nav: [
      { title: 'Funkcja liniowa', id: '#LinearFunction' },
      { title: 'Funkcja kwadratowa', id: '#SquareFunction' }
    ]
  }),
  mounted() {
    new Chartist.Line('.ct-chart-1', {
      labels: this.students.map(v => v.name),
      series: [this.students.map(v => v.v)]
    }, {
      height: 300,
      showLine: false,
      fullWidth: true
    });
  }
}
</script>

<style scoped>
</style>
