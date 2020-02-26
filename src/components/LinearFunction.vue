<template>
  <v-container>
    <h2 class="headline pb-4">Funkcja liniowa</h2>

    <v-alert border="left" colored-border color="red">
      <div class="title">
        Definicja
      </div>
      <div>
        Funkcję liniową określamy wzorem <b>f(x) = ax + b</b> dla <b>x &isin; R</b>, gdzie <b>a</b> i <b>b</b> są stałymi.
      </div>
    </v-alert>
    <!-- dziedzina -->
    <p>
      Aby obliczyć wartość funkcji dla danego argumentu, podstawiamy go do wzoru jako <b>x</b>. Przykładowo, gdy mamy taką funkcję: <code>f(x) = 2x + 1</code> to dla argumentu równego <b>2</b> wyliczymy jej wartość w następujący sposób: <code>f(2) = 2*2 + 1 = 5</code>.
    </p>
    <p>
      Gdy chcielibyśmy narysować funkcję liniową wystarczy, że wyliczymy dowolne dwa punkty, zaznaczymy je na układzie współrzędnych, a następnie poprowadzimy linię prostą przechodzącą przez obydwa te punkty.
    </p>
    <p>
      Wartość funkcji dla argumentu <b>2</b> mamy już wyliczoną, policzmy zatem wartość dla argumentu <b>-2</b>, aby móc ją narysować: <code>f(-2) = 2*(-2) + 1 = -3</code>. Zatem nasza funkcja będzie prezentowała się następująco:
    </p>
    <div class="ct-chart-11"></div>
    <h3 class="title pt-4">Współczynnik kierunkowy</h3>
    <p>
      Stała <b>a</b> nazywana jest również współczynnikiem kierunkowym, ponieważ od jej wartości zależy to, w którym kierunku będzie biegł wykres funkcji. Przykładowo, gdy jest to liczba dodatnia, to rosnący <b>x</b>, pomnożony przez nią będzie dawał rosnący wykres funkcji. Natomiast gdy współczynnik kierunkowy będzie ujemny, to zamieni nam znak iksa na przeciwny, tym samym sprawi, że wykres funkcji będzie malejący. Natomiast gdy pod <b>a</b> wstawimy zero, to otrzymamy tak zwaną funkcję stałą (jej wartość się nie zmienia).
    </p>
    <p>
      Możemy to sprowadzić do prostej zasady:
    </p>
    <v-alert border="left" colored-border color="red">
      <div>
        Gdy <b>a &gt; 0</b> to funkcja jest rosnąca.<br>
        Gdy <b>a &lt; 0</b> to funkcja jest malejąca.<br>
        Gdy <b>a = 0</b> to funkcja jest stała.<br>
      </div>
    </v-alert>
    <p>
      Weźmy na przykład takie trzy funkcje: <code>f(x) = 1x + 2</code>, <code class="purple--text">f(x) = -1x + 2</code>, <code class="orange--text">f(x) = 0x + 2</code>
    </p>
    <div class="ct-chart-10"></div>
    <p>
      Możemy tu również łatwo zaobserwować, że im większa jest wartość bezwzględna z współczynnika kierunkowego tym kąt nachylenia wykresu funkcji jest większy.
    </p>
    <h3 class="title pt-4">Współczynnik b</h3>
    <p>
      Współczynnik b nazywany również wyrazem wolnym, jest miejscem w którym funkcja przecina oś <b>y</b>. Dla przykładu: jeśli wyraz wolny miałby wartość <b>b = 8</b>, to wiemy że nasza funkcja będzie przecinała oś <b>y</b> w miejscu <b>y = 8</b>. Z perspektywy rysowania wykresu funkcji, zmienna ta odpowiada za przesunięcie w pionie. Jeśli <b>b</b> jest dodatnie to przesuwa wykres funkcji "do góry", a gdy jest ujemne przesuwa ją "w dół".
    </p>
    <h3 class="title pt-4">Miejsce zerowe</h3>
    <p>
      Miejsce zerowe funkcji to argument dla którego funkcja przyjmuje wartość zero. Na wykresie funkcji będzie to miejsce w którym funkcja przecina oś <b>x</b> (czyli tam gdzie <b>y</b> jest równy zero).
    </p>
    <p>
      Pierwszym sposobem na wyznaczenie miejsca zerowego funkcji liniowej jest przyrównanie jej wzoru do zera. Dla funkcji <code>f(x) = 1x + 2</code> równanie będzie wyglądało następująco: <code>1x + 2 = 0</code>. Po rozwiązaniu okarze się, że mejscem zerowym tej funkcji jest <b>-2</b>. Zgadza się to z powyższym wykresem (jest ona narysowana kolorem <span class="red--text">czerwonym</span>).
    </p>
    <p>
      Drugim sposobem jest skożystanie ze wzoru: <code>x<sub>0</sub> = -(b/a)</code>. Po podstawieniu dostaniemy ten sam wynik: <code>x<sub>0</sub> = -(2/1) = -2</code>
    </p>
    <h3 class="title pt-4">Plac zabaw</h3>
    <p>
      Zmodyfikuj parametry funkcji liniowej przesuwając suwakami i zobacz jak będzie ona wyglądała.
    </p>
    <v-row>
      <v-col cols="8">
        <div class="ct-chart-12"></div>
      </v-col>
      <v-col>
        <div class="pa-4 mt-4">
          <p class="text-center pb-10">
            <code>f(x) = {{ sliderA }}x {{ ((sliderB >= 0) ? '+' : '-') }} {{ Math.abs(sliderB) }}</code>
            <br><br>
            <code>x<sub>0</sub>{{ ((sliderA != 0)? ` = -(${pgB}/${pgA})` : '') }} = {{ pgZero }}</code>
          </p>
          <v-slider class="pb-4 pt-10" color="red darken-2" track-color="red lighten-2" v-model="sliderA" thumb-label="always" label="a =" :min="-3" :max="3" :step="0.2"></v-slider>
          <v-slider color="red darken-2" track-color="red lighten-2" v-model="sliderB" thumb-label="always" label="b =" :min="-3" :max="3" :step="0.2"></v-slider>
        </div>
      </v-col>
    </v-row>
    <h3 class="title pt-4">Zastosowanie funkcji liniowej</h3>
    <p>
      Zastanówmy się teraz do jakich celów można w praktyce wykorzystać funkcję liniową. Często przydają się one do dokonywania analizy przebiegu zjawisk w czasie. Możemy dzięki nim badać zależność między różnymi danymi, porównywać je ze sobą, a nawet na ich podstawie dokonywać prognozowania.
    </p>
    <p>
      Weźmy na przykład firmę transportową, która swoje usługi wycenia między innymi na podstawie dystansu na jaki trzeba dany towar przewieźć. Cena usługi to suma stałych kosztów transportu oraz danej stawki za każdy przejechany kilometr. Taki sposób wyceniania można opisać przykładową funkcją: <code>f(x) = 4,15x + 500</code>, gdzie niewiadoma <b>x</b> to ilość kilometrów mnożona przez <b>4,15</b>, czyli cenę za kilometr, a <b>500</b> to stałe koszty przewozu. Ustalając taką funkcję, jesteśmy w stanie określić cenę dla każdego możliwego przewozu.
    </p>
    <p>
      Innym przykładem może być firma produkująca ręcznie robione stroiki. Ponosi ona codzienne koszty (wypłaty pracowników, zakup materiałów, prąd potrzebny do działania linii produkcyjnej itp.). Możemy je opisać funkcją liniową <code class="purple--text">f(x) = x + 60</code>. Codziennie stroiki sprzedawane są w lokalnym sklepie, a poza tym prowadzony jest sklep internetowy. Zysk z każdego sprzedanego stroika można opisać funkcją: <code>f(x) = 3x</code>. Zobaczmy, jak będą one wyglądały:
    </p>
    <div class="ct-chart-13"></div>
    <p>
      Poprzez narysowanie wykresów obu tych funkcji i ich porównanie możemy wywnioskować, że aby dochód ze sprzedaży towaru pokrył koszty produkcji, należy sprzedać co najmniej 30 stroików dziennie (jest to miejsce w którym obie funkcje się przecinają).
    </p>
    <v-divider></v-divider>
  </v-container>
</template>

<script>
import Chartist from 'chartist'

export default {
  data() {
    return {
      xs: Array.from(Array(11).keys()).map(x => x-5),
      sliderA: 0,
      sliderB: 0,
      pgChart: null
    };
  },
  computed: {
    pgB() {
      return (this.sliderB >= 0) ? this.sliderB : `(${this.sliderB})`;
    },
    pgA() {
      return (this.sliderA >= 0) ? this.sliderA : `(${this.sliderA})`;
    },
    pgZero() {
      return ((this.sliderA != 0)? (-(this.sliderB/this.sliderA)).toFixed(2) : 0);
    },
    pgF() {
      return this.xs.map(x => ({ x: x, y: this.linear(x, this.sliderA, this.sliderB)}));
    }
  },
  methods: {
    linear: (x, a, b) => a*x + b,
    chart1() {
      const f1 = this.xs.map(x => this.linear(x, 1, 2));
      const f2 = this.xs.map(x => this.linear(x, -1, 2));
      const f3 = this.xs.map(x => this.linear(x, 0, 2));

      new Chartist.Line('.ct-chart-10', {
        labels: this.xs,
        series: [f1, f2, f3]
      }, {
        height: 350,
        showPoint: false,
        fullWidth: true
      });
    },
    chart2() {
      const f1 = this.xs.map(x => this.linear(x, 2, 1));
      const f2 = this.xs.map(x => (x == -2 || x == 2) ? this.linear(x, 2, 1) : null);

      new Chartist.Line('.ct-chart-11', {
        labels: this.xs,
        series: [{
          name: 'f1',
          data: f1
        }, {
          name: 'f2',
          data: f2
        }]
      }, {
        series: {
          f1: {
            showPoint: false
          },
          f2: {
            showLine: false
          }
        },
        height: 300,
        fullWidth: true
      });
    },
    chart3() {
      this.pgChart = new Chartist.Line('.ct-chart-12', {
        labels: this.xs,
        series: [{
          name: 'series-function',
          data: this.pgF
        }]
      }, {
        series: {
          'series-function': {
            showPoint: false
          }
        },
        height: 500,
        fullWidth: true,
        axisY: {
          type: Chartist.FixedScaleAxis,
          ticks: Array.from(Array(21).keys()).map(x => x-10),
          low: -10,
          high: 10
        }
      });
    },
    chart4() {
      const xs = Array.from(Array(50).keys());
      const f1 = xs.map(x => this.linear(x, 3, 0));
      const f2 = xs.map(x => this.linear(x, 1, 60));

      new Chartist.Line('.ct-chart-13', {
        labels: xs,
        series: [{
          name: 'f1',
          data: f1
        }, {
          name: 'f2',
          data: f2
        }]
      }, {
        showPoint: false,
        height: 300,
        fullWidth: true
      });
    },
  },
  watch: {
    pgF() {
      this.pgChart.update({
        labels: this.xs,
        series: [{
          name: 'series-function',
          data: this.pgF
        }]
      });
    }
  },
  mounted() {
    this.chart1();
    this.chart2();
    this.chart3();
    this.chart4();
  }
}
</script>

<style>
.ct-chart-10 .ct-series-a .ct-line,
.ct-chart-10 .ct-series-a .ct-point {
  stroke: red;
}
.ct-chart-10 .ct-series-b .ct-line,
.ct-chart-10 .ct-series-b .ct-point {
  stroke: purple;
}
.ct-chart-10 .ct-series-c .ct-line,
.ct-chart-10 .ct-series-c .ct-point {
  stroke: orange;
}

.ct-chart-11 .ct-series-b .ct-point {
  stroke: black;
}

.ct-chart-12 .ct-grids .ct-grid.ct-vertical:nth-child(22),
.ct-chart-12 .ct-grids .ct-grid.ct-horizontal:nth-child(6) {
  stroke: #000;
  stroke-dasharray: 0px;
}

.ct-chart-13 .ct-series-b .ct-line {
  stroke: purple;
}
</style>
