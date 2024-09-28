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
  <hr class="header-line" />
</template>

<script>
export default {
  name: "HeaderView",
};
</script>

<style scoped>
header {
  background-color: #42b983;
  margin-top: -1rem;
  padding: 1rem 2rem;
  top: 0;
  margin-left: -2rem;
  width: 100%;
  z-index: 1000;
}
.header-line {
  border: none;
  border-top: 0.1px solid #ffffff;
  margin: 0;
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
  margin-right: 2rem;
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
