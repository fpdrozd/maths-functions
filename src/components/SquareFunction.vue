<template>
  <v-container>
    <h2 class="headline pb-4">Funkcja kwadratowa</h2>
    <p>
      Funkcja kwadratowa jest jedną z najpopularniejszych funkcji, zaraz obok funkcji liniowej. Różni się jednak od niej tym, że dodatkowo niewiadoma <b>x</b> jest podniesiona do potęgi. Jak sama nazwa wskazuje w funkcji kwadratowej niewiadoma <b>x</b> podnoszona jest do kwadratu, stąd też nazywamy ją <b>trójmianem kwadratowym</b>.
    </p>
    <v-alert border="left" colored-border color="red">
      <div class="title">
        Definicja
      </div>
      <div>
        Postać: <b>f(x) = ax<sup>2</sup> + bx + c</b>, gdzie a &#8800; 0 nazywamy <b>postacią ogólną</b> funkcji kwadratowej. <br>
        Postać: <b>f(x) = a(x - p)<sup>2</sup> + q</b>, gdzie a &#8800; 0 nazywamy <b>postacią kanoniczną</b> funkcji kwadratowej. <br>
        Postać: <b>f(x) = a(x - x<sub>1</sub>)(x - x<sub>2</sub>)</b>, gdzie a &#8800; 0 nazywamy <b>postacią iloczynową</b> (istnieje ona tylko wtedy, gdy funkcja kwadratowa ma miejsca zerowe)
      </div>
    </v-alert>
    <p>
      Wykresem funkcji kwadratowej jest parabola. Poniżej przedstawiony jest wykres funkcji <code>f(x) = x<sup>2</sup></code>:
    </p>
    <div class="ct-chart-20"></div>
    <h3 class="title pt-4">Współczynnik a</h3>
    <p>
      W funkcji kwadratowej występuje stała <b>a</b>, która jest odpowiednikiem współczynnika kierunkowego w funkcji liniowej. Decyduje ona o tym, czy ramiona paraboli będą skierowane do góry, czy do dołu.
    </p>
    <v-alert border="left" colored-border color="red">
      <div>
        Gdy <b>a &gt; 0</b> to ramiona paraboli będą skierowane do góry.<br>
        Gdy <b>a &lt; 0</b> to ramiona paraboli będą skierowane do dołu.<br>
      </div>
    </v-alert>
    <p>
      Weźmy na przykład takie dwie funkcje: <code class="purple--text">f(x) = 1x<sup>2</sup></code>, <code class="orange--text">f(x) = -1x<sup>2</sup></code>
    </p>
    <v-row>
      <v-col>
        <div class="ct-chart-21"></div>
      </v-col>
      <v-col>
        <div class="ct-chart-22"></div>
      </v-col>
    </v-row>
    <h3 class="title">Postać ogólna</h3>
    <p>
      <code>f(x) = ax<sup>2</sup> + bx + c</code>
    </p>
    <p>
      Zaletami postaci ogólnej jest to, że od razu możemy odczytać, kierunek ułożenia ramion paraboli. Ponadto z łatwością możemy odczytać miejsce przecięcia się paraboli z osią igreków, spoglądając na współczynnik <b>c</b>. Przykładowo, gdy <b>c = 3</b>, to funkcja przetnie oś igreków dla <b>y = 3</b>.
    </p>
    <p>
      Aby obliczyć współrzędne wierzchołka funkcji kwadratowej, zwanego również ogniskiem paraboli <b>W = (p;q)</b>, kożystamy ze wzorów: <code>p = (-b)/2a</code> oraz <code>q = (-&#916;)/4a</code>.
    </p>
    <h4 class="subtitle-1 font-weight-bold">Miejsca zerowe</h4>
    <p>
      Miejsce zerowe funkcji to argument dla którego funkcja przyjmuje wartość zero. Łatwo zauważyć, że w przypadku funkcji kwadratowej jeśli w ogóle będziemy mieli miejsca zerowe, to będzie ich dwa (w przypadku gdy oba ramiona będą przecinały oś <b>x</b>), lub jedno nazywane pierwiastkiem podwójnym (gdy wierzchołek funkcji będzie położony na osi <b>x</b>).
    </p>
    <p>
      Aby obliczyć miejsca zerowe możemy skorzystać z delty.
    </p>
    <v-alert border="left" colored-border color="red">
      <div class="pb-2">
        Deltę wyznaczamy korzystając ze wzoru: <b>&#916; = b<sup>2</sup> - 4ac</b>
      </div>
      <div class="pb-2">
        Jeśli <b>&#916; &gt; 0</b>, to trójmian posiada dwa miejsca zerowe i można przedstawić ją w postaci iloczynowej <b>f(x) = a(x - x<sub>1</sub>)(x - x<sub>2</sub>)</b>, gdzie <b>x<sub>1</sub></b>, <b>x<sub>2</sub></b> są pierwiastkami tego trójmianu.
      </div>
      <div class="pb-2">
        Jeśli <b>&#916; = 0</b>, to trójmian można przedstawić w postaci iloczynowej <b>f(x) = a(x - x<sub>0</sub>)<sup>2</sup></b>, gdzie <b>x<sub>0</sub></b> jest pierwiastkiem podwójnym tego trójmianu.
      </div>
      <div>
        Jeśli <b>&#916; &lt; 0</b>, to trójmianu nie można rozłożyć na czynniki liniowe.
      </div>
    </v-alert>
    <v-row>
      <v-col>
        <p>
          Weźmy za przykład taką funkcję: <code>f(x) = 1x<sup>2</sup> + 6x + 5</code>. Obliczamy deltę korzystając ze wzoru: <code>&#916; = 6<sup>2</sup> - 4*1*5 = 16</code>. Delta wyszła większa niż zero, znaczy to że równanie kwadratowe ma dwa pierwiastki. Obliczymy je korzystając ze wzorów: <code>x<sub>1</sub> = (-b - &#8730;&#916;)/2a</code>, <code>x<sub>2</sub> = (-b + &#8730;&#916;)/2a</code>. Zatem: <code>x<sub>1</sub> = (-6 - 4)/2 = -5</code>, <code>x<sub>2</sub> = (-6 + 4)/2 = -1</code>.
        </p>
      </v-col>
      <v-col>
        <div class="ct-chart-23"></div>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <div class="ct-chart-24"></div>
      </v-col>
      <v-col>
        <p>
          W przypadku gdy delta nam wyjdzie równa zero, jedynym pierwiastkiem funkcji jest jej wierzchołek. Wyliczamy go więc w następujący sposób: <code>x<sub>0</sub> = (-b)/2a</code>. Dla przykładu, mamy taką funkcję: <code>f(x) = 1x<sup>2</sup> + 4x + 4</code>. Wyliczamy deltę: <code>&#916; = 4<sup>2</sup> - 4*1*4 = 0</code>. Faktycznie jest ona równa zero, tak więc jedynym pierwiastkiem tej funkcji jest: <code>x<sub>0</sub> = (-4)/2 = -2</code>.
        </p>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <p>
          Ostatnim przypadkiem jest ten w którym delta wychodzi ujemna. Zobaczmy przykładową funkcję: <code>f(x) = 1x<sup>2</sup> + 2x + 4</code>. Liczymy deltę: <code>&#916; = 2<sup>2</sup> - 4*1*4 = -12</code>. Faktycznie wychodzi ujemna, więc nie ma ona miejsc zerowych. Zobaczmy wykres:
        </p>
      </v-col>
      <v-col>
        <div class="ct-chart-25"></div>
      </v-col>
    </v-row>
    <h3 class="title pt-4">Postać kanoniczna</h3>
    <p>
      <code>f(x) = a(x - p)<sup>2</sup> + q</code>
    </p>
    <p>
      Z postaci kanonicznej funkcji kwadratowej z łatwością możemy odczytać współrzędne wierzchołka <b>W = (p;q)</b>. Trzeba jednak zwrócić uwagę na znak stojący przed <b>p</b>. Dla przykładu, gdy mamy taką funkcję: <code>f(x) = 1(x - 2)<sup>2</sup> + 4</code>, to współrzędnymi wierzchołka będą <b>W = (2;4)</b>. Łatwo jest się tu pomylić i zapisać pierwszą współrzędną jako <b>-2</b>. Dla funkcji: <code>f(x) = 1(x + 3)<sup>2</sup> - 1</code>, współrzędne wierzchołka będą wyglądały tak: <b>W = (-3;-1)</b>.
    </p>
    <p>
      Z postaci kanonicznej możemy również w łatwy sposób przejść na inną postać, na przykład ogólną.
    </p>
    <h4 class="subtitle-1 font-weight-bold">Przekształcenie do postaci ogólnej</h4>
    <p>
      Aby przekształcić funkcję zapisaną w postaci kanonicznej do postaci ogólnej musimy skorzystać ze wzoru skróconego mnożenia. Weźmy za przykład taką funkcję: <code>f(x) = 2(x - 4)<sup>2</sup> - 5</code>. Korzystając ze wzoru skróconego mnożenia <code>(a - b)<sup>2</sup> = a<sup>2</sup> - 2ab + b<sup>2</sup></code>, możemy zapisać ją w następujący sposób: <code>f(x) = 2(x<sup>2</sup> - 8x + 4<sup>2</sup>) - 5</code>. Po wyliczeniu otrzymamy wzór funkcji zapisany w postaci ogólnej: <code>f(x) = 2x<sup>2</sup> - 16x + 27</code>.
    </p>
    <p>
      Jako drugi przykład weźmy taką funkcję: <code>f(x) = 3(x + 1)<sup>2</sup> - 6</code>. Tym razem użyjemy wzoru na kwadrat sumy: <code>(a + b)<sup>2</sup> = a<sup>2</sup> + 2ab + b<sup>2</sup></code>. Po użyciu wzoru skróconego mnożenia funkcja będzie wyglądała następująco: <code>f(x) = 3(x<sup>2</sup> + 2x + 1) - 6</code>. Po wymnożeniu również otrzymamy naszą funkcję w postaci ogólnej: <code>f(x) = 3x<sup>2</sup> + 6x - 3</code>.
    </p>
    <h3 class="title pt-4">Postać iloczynowa</h3>
    <p>
      <code>f(x) = a(x - x<sub>1</sub>)(x - x<sub>2</sub>)</code>
    </p>
    <p>
      Zaletami postaci iloczynowej jest to, że od razu widzimy miejsca zerowe (<b>x<sub>1</sub></b> oraz <b>x<sub>2</sub></b>). Aby to zrobić należy przyrównać wartość każdego z nawiasów do zera i wyliczyć iksa. Za zwyczaj jednak wystarczy spojrzeć i od razu widać, że przykładowo <b>(x - 4)</b> wyzeruje się dla <b>x = 4</b>, a <b>(x + 5)</b> dla <b>x = -5</b>.
    </p>
    <h4 class="subtitle-1 font-weight-bold">Przekształcenie do postaci ogólnej</h4>
    <p>
      Gdy zobaczymy funkcję zapisaną w postaci iloczynowej: <code>f(x) = (x - 2)(x - 3)</code> to na pierwszy rzut oka nie wygląda ona na funkcję kwadratową, gdyż nie widzimy iksa podniesionego do potęgi. Jednak łatwo możemy przekształcić ją wymnażając nawiasy: <code>f(x) = (x - 2)(x - 3) = x<sup>2</sup> - 3x - 2x + 6</code>. Po zredukowaniu otrzymamy wzór funkcji zapisany w postaci ogólnej: <code>f(x) = x<sup>2</sup> - 5x + 6</code>.
    </p>
    <h3 class="title pt-4">Plac zabaw</h3>
    <p>
      Zmodyfikuj parametry funkcji kwadratowej przesuwając suwakami i zobacz jak będzie ona wyglądała.
    </p>
    <v-row>
      <v-col cols="8">
        <div class="ct-chart-26"></div>
      </v-col>
      <v-col>
        <div class="calculations pa-4 mt-4">
          <div>
            <code class="mb-8">f(x) = {{ sliderA }}x<sup>2</sup> {{ ((sliderB >= 0) ? '+' : '-') }} {{ Math.abs(sliderB) }}x {{ ((sliderC >= 0) ? '+' : '-') }} {{ Math.abs(sliderC) }}</code>
          </div>
          <div>
            <code class="mb-4 orange--text" v-if="sliderA != 0">&#916; = ({{ sliderB }})<sup>2</sup> - 4*{{ (sliderA >= 0)? sliderA : `(${sliderA})` }}*{{ (sliderC >= 0)? sliderC : `(${sliderC})` }} = {{ pgDelta }}</code>
          </div>
          <div>
            <code class="mb-4 purple--text" v-if="sliderA != 0 && pgDelta == 0">x<sub>0</sub> = -{{ (sliderB >= 0)? sliderB : `(${sliderB})` }}/2*{{ (sliderA >= 0)? sliderA : `(${sliderA})` }} = {{ pgZero1 }}</code>
          </div>
          <div>
            <code class="mb-4 purple--text" v-if="pgDelta > 0 && sliderA != 0">x<sub>1</sub> = (-{{ (sliderB >= 0)? sliderB : `(${sliderB})` }} - &#8730;{{ pgDelta }})/2*{{ (sliderA >= 0)? sliderA : `(${sliderA})` }} = {{ pgZero1 }}</code>
          </div>
          <div>
            <code class="mb-4 purple--text" v-if="pgDelta > 0 && sliderA != 0">x<sub>2</sub> = (-{{ (sliderB >= 0)? sliderB : `(${sliderB})` }} + &#8730;{{ pgDelta }})/2*{{ (sliderA >= 0)? sliderA : `(${sliderA})` }} = {{ pgZero2 }}</code>
          </div>
          <div>
            <code class="mb-4 green--text" v-if="sliderA != 0">p = (-{{ ((sliderB >= 0)? sliderB : `(${sliderB})`) }})/2*{{ ((sliderA >= 0)? sliderA : `(${sliderA})`) }} = {{ ((-sliderB)/(2*sliderA)).toFixed(2) }}</code>
          </div>
          <div>
            <code class="mb-4 green--text" v-if="sliderA != 0">q = (-{{ ((pgDelta >= 0)? pgDelta : `(${pgDelta})`) }})/4*{{ ((sliderA >= 0)? sliderA : `(${sliderA})`) }} = {{ ((-pgDelta)/(4*sliderA)).toFixed(2) }}</code>
          </div>
        </div>
      </v-col>
    </v-row>
    <v-row class="pt-6">
      <v-col cols="4">
        <v-slider color="red darken-2" track-color="red lighten-2" v-model="sliderA" thumb-label="always" label="a =" :min="-6" :max="6" :step="0.2"></v-slider>
      </v-col>
      <v-col cols="4">
        <v-slider color="red darken-2" track-color="red lighten-2" v-model="sliderB" thumb-label="always" label="b =" :min="-6" :max="6" :step="0.2"></v-slider>
      </v-col>
      <v-col cols="4">
        <v-slider color="red darken-2" track-color="red lighten-2" v-model="sliderC" thumb-label="always" label="c =" :min="-3" :max="3" :step="0.2"></v-slider>
      </v-col>
    </v-row>
    <h3 class="title pt-4">Zastosowanie funkcji kwadratowej</h3>
    <p>
      Zastanówmy się teraz, do jakich celów można w praktyce wykorzystać funkcję kwadratową. Przykładem zastosowania w geometrii są klasyczne zadania typu: Z kartki papieru (o konkretnych wymiarach) wycinamy na rogach kwadraty jednakowych rozmiarów, tak aby po sklejeniu otrzymać otwarte pudełko. Następnie należy podać dla jakiej długości boku owego kwadratu, pole powierzchni bocznej pudełka będzie największe. Pole powierzchni bocznej możemy wtedy opisać funkcją kwadratową, gdzie <b>x</b> to długość boku odcinanych kwadratów. Największą wartością tej funkcji jest wierzchołek paraboli, który trzeba tylko policzyć.
    </p>
    <p>
      Innym ciekawym przykładem może być firma produkująca kurtki. Koszt wyprodukowania jednej kurtki to 80 zł, natomiast cena, po jakiej jest ona sprzedawana to 100 zł. Wiadomo, że przy tej cenie sprzedawanych jest 100 kurtek na miesiąc oraz że każdorazowe podniesienie ceny kurtki o 10 zł powoduje spadek sprzedaży o 5 sztuk. Analogicznie do poprzedniego przykładu, należy podać liczbę podwyżek ceny o 10 zł, dla której miesięczny zysk będzie największy.
    </p>
    <p>
      Rozwiążmy to zadanie. Zysk ze sprzedaży jednej kurtki możemy opisać jako <code>20 + 10x</code>, gdzie <b>20</b> oznacza aktualny zysk (<b>&lt;cena kurtki&gt; - &lt;koszt wyprodukowania&gt;</b>), a <b>x</b> to liczba podwyżek ceny o 10 zł. Musimy teraz ten zysk pomnożyć przez liczbę sprzedanych kurtek. Wiemy jednak, że ona również jest zależna od ilości podwyżek. Zapiszemy to więc w następujący sposób: <code>100 - 5x</code>, gdzie <b>100</b> oznacza aktualną liczbę miesięcznie sprzedawanych kurtek, a <b>5x</b> to spadek sprzedaży o 5 sztuk przy każdej podwyżce, który odejmujemy.
    </p>
    <p>
      Zatem funkcja opisująca miesięczny zysk będzie wyglądała następująco: <code>f(x) = (20 + 10x)(100 - 5x)</code>. Po wymnożeniu nawiasów otrzymamy ją w postaci ogólnej: <code>f(x) = -50x<sup>2</sup> + 900x + 200</code>. Największą wartością tej funkcji jest miejsce, w którym znajduje się jej wierzchołek. Możemy zatem wyliczyć jego parametry w znany nam już sposób: <code class="orange--text">&#916; = 900<sup>2</sup> - 4*(-50)*200 = 850000</code>, <code class="green--text">p = (-900)/2*(-50) = 9</code>, <code class="green--text">q = (-850000)/4*(-50) = 4250</code>
    </p>
    <div class="ct-chart-27"></div>
    <p>
      Wiemy zatem, że największy miesięczny zysk możliwy do uzyskania to <b>4250 zł</b>, który osiągniemy, podnosząc cenę kurtki <b>9 razy</b> o 10 zł, czyli o <b>90 zł</b>. W związku z tym nowa cena kurtki będzie wynosiła <b>190 zł</b>, co swoją drogą jest niezłym interesem.
    </p>
    <v-divider></v-divider>
  </v-container>
</template>

<script>
import Chartist from 'chartist'

export default {
  data() {
    return {
      xs: Array.from(Array(21).keys()).map(x => x-10),
      xs11_7: Array.from(Array(11).keys()).map(x => x-7),
      xsHalf: Array.from(Array(21).keys()).map(x => (x/4)-2.5),
      pgChart: null,
      sliderA: 0,
      sliderB: 0,
      sliderC: 0
    };
  },
  methods: {
    square: (x, a, b, c) => a*x*x + b*x + c,
    chart1() {
      const f1 = this.xs.map(x => this.square(x, 1, 0, 0));

      new Chartist.Line('.ct-chart-20', {
        labels: this.xs,
        series: [f1]
      }, {
        height: 300,
        showPoint: false,
        fullWidth: true
      });
    },
    chart2() {
      const f1 = this.xs.map(x => this.square(x, 1, 0, 0));

      new Chartist.Line('.ct-chart-21', {
        labels: this.xs,
        series: [f1]
      }, {
        height: 300,
        showPoint: false,
        fullWidth: true
      });
    },
    chart3() {
      const f1 = this.xs.map(x => this.square(x, -1, 0, 0));

      new Chartist.Line('.ct-chart-22', {
        labels: this.xs,
        series: [f1]
      }, {
        height: 300,
        showPoint: false,
        fullWidth: true
      });
    },
    chart4() {
      const f1 = this.xs11_7.map(x => this.square(x, 1, 6, 5));
      const f2 = this.xs11_7.map(x => (x == -5 || x == -1)? this.square(x, 1, 6, 5) : null);

      new Chartist.Line('.ct-chart-23', {
        labels: this.xs11_7,
        series: [{
          name: 'f1',
          data: f1
        },{
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
        height: 200,
        fullWidth: true
      });
    },
    chart5() {
      const f1 = this.xs11_7.map(x => this.square(x, 1, 4, 4));
      const f2 = this.xs11_7.map(x => (x == -2)? this.square(x, 1, 4, 4) : null);

      new Chartist.Line('.ct-chart-24', {
        labels: this.xs11_7,
        series: [{
          name: 'f1',
          data: f1
        },{
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
        height: 200,
        fullWidth: true
      });
    },
    chart6() {
      const f1 = this.xs11_7.map(x => this.square(x, 1, 2, 4));

      new Chartist.Line('.ct-chart-25', {
        labels: this.xs11_7,
        series: [f1]
      }, {
        showPoint: false,
        height: 200,
        fullWidth: true
      });
    },
    chart7() {
      this.pgChart = new Chartist.Line('.ct-chart-26', {
        labels: this.xsHalf,
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
    chart8() {
      const xs = Array.from(Array(26).keys()).map(x => (x-4));
      const f1 = xs.map(x => this.square(x, -50, 900, 200));
      const f2 = xs.map(x => (x == 9)? this.square(x, -50, 900, 200) : null);

      new Chartist.Line('.ct-chart-27', {
        labels: xs,
        series: [{
          name: 'f1',
          data: f1
        },{
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
        height: 450,
        fullWidth: true
      });
    },
  },
  computed: {
    pgF() {
      return this.xsHalf.map(x => ({ x: x, y: this.square(x, this.sliderA, this.sliderB, this.sliderC)}));
    },
    pgDelta() {
      return (this.sliderB*this.sliderB - 4*this.sliderA*this.sliderC).toFixed(2);
    },
    pgZero1() {
      return (((-this.sliderB)-Math.sqrt(this.pgDelta))/(2*this.sliderA)).toFixed(2);
    },
    pgZero2() {
      return (((-this.sliderB)+Math.sqrt(this.pgDelta))/(2*this.sliderA)).toFixed(2);
    }
  },
  watch: {
    pgF() {
      this.pgChart.update({
        labels: this.xsHalf,
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
    this.chart5();
    this.chart6();
    this.chart7();
    this.chart8();
  }
}
</script>

<style>
.ct-chart-21 .ct-series-a .ct-line,
.ct-chart-21 .ct-series-a .ct-point {
  stroke: purple;
}
.ct-chart-22 .ct-series-a .ct-line,
.ct-chart-22 .ct-series-a .ct-point {
  stroke: orange;
}
.ct-chart-23 .ct-series-b .ct-point,
.ct-chart-24 .ct-series-b .ct-point,
.ct-chart-27 .ct-series-b .ct-point {
  stroke: black;
}

.ct-chart-26 .ct-grids .ct-grid.ct-vertical:nth-child(32),
.ct-chart-26 .ct-grids .ct-grid.ct-horizontal:nth-child(11),
.ct-chart-27 .ct-grids .ct-grid.ct-vertical:nth-child(36),
.ct-chart-27 .ct-grids .ct-grid.ct-horizontal:nth-child(5) {
  stroke: #000;
  stroke-dasharray: 0px;
}
</style>
