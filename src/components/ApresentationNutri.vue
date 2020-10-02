<template>
  <div id="section-apresentatin-nutri">
    <b-row class="apresentation-nutri">
      <b-col cols="6" class="box-side">
        <p class="Nutri title">Samuel Rodrigues</p>
        <p class="Nutri">
          Oi, eu sou o Samuel, uma apaixonada por pesquisa, ensino, atendimento
          clínico e tudo que envolve alimentação, nutrição e saúde.
        </p>
        <!-- <p>
          Defendi meu doutorado em fisiopatologia pela faculdade de medicina da
          UERJ/Utah University em 2009. Sou especialista em Nutrição clínica
          (UFRJ) e Certificada pela American College of Lifestyle Medicine.
          Hoje, atuo professora adjunta de nutrição clínica da Universidade do
          Estado do Rio de Janeiro (UERJ) e sou pesquisadora do Instituto
          Nacional de Cardiologia (INC), locais onde tenho oportunidade de
          realizar pesquisa clínica em nutrição há mais de 15 anos.
        </p> -->
        <p class="Nutri">
          Faço atendimento clínico e ministro palestras para grandes
          universidades e congressos em todo o Brasil.
        </p>
        <p class="Nutri">
          Hoje, me completo nos meus 3 pilares: Atendimento, docência e
          pesquisa.
        </p>
        <p class="Nutri">
          Neste espaço você encontrará informações sobre atendimento clínico,
          materiais gratuitos, livros e cursos para profissionais da saúde.
        </p>

        <p class="Nutri">Seja bem-vindo(a)!</p>
      </b-col>
      <b-col cols="6" class="box-side">
        <div class="imagem-nutri"></div>
      </b-col>
    </b-row>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({});
</script>

<style lang="scss" scoped>
.apresentation-nutri {
  display: block;
  margin: 0 auto;
  width: 1200px;
  height: 600px;
}

.box {
  background: #8bc740;
}

.box-side {
  width: 50%;
  height: 100%;
  padding: 68px 68px;
  float: left;
}

.imagem-nutri {
  width: 100%;
  height: 100%;
  background: url(../assets/img/doutorFitness.jpg);
}

#section-apresentatin-nutri {
  background: #8bc740;
}

.Nutri {
  float: none;
  display: block;
  text-align: start;
  font-family: "Quicksand", sans-serif;
  color: #fff;

  &.title {
    font-size: 34px;
  }
}
</style>