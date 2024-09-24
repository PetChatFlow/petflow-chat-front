<template>
  <div class="produto-card">
    <h3>{{ produto.nome }}</h3>
    <p class="preco">R$ {{ produto.preco.toFixed(2) }}</p>
    <button>Adicionar ao Carrinho</button>
  </div>
</template>

<script>
export default {
  name: "ProdutoCard",
  props: {
    produto: Object,
  },
};
</script>

<style scoped>
.produto-card {
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 1rem;
  text-align: center;
}

.produto-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 1rem;
}

.preco {
  font-weight: bold;
  color: #42b983;
  margin-bottom: 1rem;
}

button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #3aa876;
}
</style>
