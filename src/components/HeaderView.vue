<template>
  <header>
    <nav>
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
  width: 100%;
  z-index: 1000;
  position: sticky;
  top: 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

.logo img {
  height: 40px;
}

.nav-links {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  justify-content: flex-end; /* Alinha os links à direita */
  flex-grow: 1; /* Permite que a lista de links ocupe o espaço disponível */
}

.nav-links li {
  margin-left: 2rem;
}

.nav-links a {
  color: #ffffff;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #1a535c;
}

@media (max-width: 768px) {
  header {
    padding: 1rem;
  }

  nav {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo {
    margin-bottom: 1rem;
  }

  .nav-links {
    flex-direction: column;
    width: 100%;
    align-items: flex-end; /* Alinha os links à direita em telas menores */
  }

  .nav-links li {
    margin-left: 0;
    margin-bottom: 0.5rem;
  }
}
</style>
