<template>
  <div class="petshop-home">
    <HeaderView />
    <CarrosselView />
    <main>
      <section class="servicos">
        <h2>Nossos Serviços</h2>
        <div class="servicos-grid">
          <ServicoCard
            v-for="servico in servicos"
            :key="servico.id"
            :servico="servico"
          />
        </div>
      </section>
      <section class="produtos">
        <h2>Produtos em Destaque</h2>
        <div class="produtos-grid">
          <ProdutoCard
            v-for="produto in produtos"
            :key="produto.id"
            :produto="produto"
          />
        </div>
      </section>
    </main>
    <FooterView />
  </div>
</template>

<script>
import HeaderView from "./HeaderView.vue";
import CarrosselView from "./CarrosselView.vue";
import ServicoCard from "./ServicoCard.vue";
import ProdutoCard from "./ProdutoCard.vue";
import FooterView from "./FooterView.vue";

import racaoPremium from "@/assets/racao-premium.jpg";
import brinquedoInterativo from "@/assets/brinquedo-interativo.jpg";
import coleiraPersonalizada from "@/assets/coleira-personalizada.jpg";
import camaOrtopedica from "@/assets/cama-ortopedica.jpg";

export default {
  name: "PetshopHome",
  components: {
    HeaderView,
    CarrosselView,
    ServicoCard,
    ProdutoCard,
    FooterView,
  },
  data() {
    return {
      servicos: [
        {
          id: 1,
          nome: "Banho e Tosa",
          icone: "fa-bath",
          descricao: "Deixe seu pet limpo e cheiroso",
        },
        {
          id: 2,
          nome: "Consultas Veterinárias",
          icone: "fa-stethoscope",
          descricao: "Cuidados médicos especializados",
        },
        {
          id: 3,
          nome: "Vacinação",
          icone: "fa-syringe",
          descricao: "Mantenha seu pet protegido",
        },
        {
          id: 4,
          nome: "Hospedagem",
          icone: "fa-home",
          descricao: "Um lar longe de casa para seu pet",
        },
      ],
      produtos: [
        {
          id: 1,
          nome: "Ração Premium",
          preco: 89.9,
          descricao: "Nutrição balanceada para seu pet",
          imagem: racaoPremium,
        },
        {
          id: 2,
          nome: "Brinquedo Interativo",
          preco: 39.9,
          descricao: "Diversão e estímulo mental",
          imagem: brinquedoInterativo,
        },
        {
          id: 3,
          nome: "Coleira Personalizada",
          preco: 29.9,
          descricao: "Estilo e segurança para seu pet",
          imagem: coleiraPersonalizada,
        },
        {
          id: 4,
          nome: "Cama Ortopédica",
          preco: 149.9,
          descricao: "Conforto e suporte para seu pet",
          imagem: camaOrtopedica,
        },
      ],
    };
  },
};
</script>

<style scoped>
.petshop-home {
  font-family: "Roboto", sans-serif;
  color: #333;
}

main {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

h2 {
  color: #4a4a4a;
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2rem;
  font-weight: bold;
}

.servicos-grid,
.produtos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

section {
  margin-bottom: 4rem;
}

@media (max-width: 768px) {
  main {
    padding: 1rem;
  }

  .servicos-grid,
  .produtos-grid {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
  }
}
</style>
