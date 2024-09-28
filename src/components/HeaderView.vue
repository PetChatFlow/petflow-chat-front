<template>
  <header>
    <nav>
      <div class="logo"></div>
      <ul class="nav-links">
        <li><a href="#home">Início</a></li>
        <li><a href="#servicos">Serviços</a></li>
        <li><a href="#produtos">Produtos</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderView",
};
</script>

<style scoped>
header {
  background-color: #42b983;
  padding: 1rem 2rem;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo img {
  height: 50px;
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-links li {
  margin-left: 2rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}
</style>
