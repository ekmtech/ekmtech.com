<script setup>
const depoimentos = [
  {
    nome: "Ana Silva",
    cargo: "CEO da TechNova",
    texto: "A EKM Tech transformou nossa presença digital. Profissionais dedicados e resultados incríveis!",
    foto: "https://randomuser.me/api/portraits/women/44.jpg",
  },
  {
    nome: "Carlos Pereira",
    cargo: "Empreendedor",
    texto: "Confiança e qualidade do começo ao fim. Recomendo para qualquer negócio que queira crescer online.",
    foto: "https://randomuser.me/api/portraits/men/32.jpg",
  },
  {
    nome: "Mariana Costa",
    cargo: "Gerente de Marketing",
    texto: "Equipe atenciosa e soluções inovadoras. Superaram nossas expectativas com o novo site.",
    foto: "https://randomuser.me/api/portraits/women/68.jpg",
  },
];
</script>

<template>
  <section class="depoimentos-section">
    <h2>O que dizem sobre nós</h2>
    <div class="depoimentos-container">
      <article v-for="(dep, index) in depoimentos" :key="index" class="depoimento-card">
        <img :src="dep.foto" :alt="`Foto de ${dep.nome}`" class="foto" />
        <p class="texto">"{{ dep.texto }}"</p>
        <p class="nome">{{ dep.nome }}</p>
        <p class="cargo">{{ dep.cargo }}</p>
      </article>
    </div>
  </section>
</template>

<style scoped>
.depoimentos-section {
  max-width: 960px;
  margin: 4rem auto;
  padding: 0 1rem;
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.depoimentos-section h2 {
  font-size: 2.8rem;
  margin-bottom: 2rem;
  color: var(--ekmtechcolor);
  font-weight: 700;
}

.depoimentos-container {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  justify-content: center;
}

.depoimento-card {
  background: white;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 8px 20px rgba(0, 73, 144, 0.15);
  max-width: 300px;
  flex: 1 1 280px;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #004990;
  font-style: italic;
}

.foto {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-bottom: 1rem;
  object-fit: cover;
  box-shadow: 0 4px 10px rgba(0, 73, 144, 0.3);
}

.texto {
  flex-grow: 1;
  font-size: 1.1rem;
  margin-bottom: 1rem;
}

.nome {
  font-weight: 700;
  font-style: normal;
  margin-bottom: 0.2rem;
}

.cargo {
  font-size: 0.9rem;
  color: #0071e3;
  font-style: normal;
}

/* Responsividade */
@media (max-width: 600px) {
  .depoimentos-container {
    flex-direction: column;
    gap: 1.5rem;
  }
}
</style>
