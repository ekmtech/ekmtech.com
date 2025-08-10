<template>
  <section class="services-cards">
    <h2>O que oferecemos</h2>
    <div class="cards-container">
      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#004990" viewBox="0 0 24 24">
            <path d="M3 4v16h18V4H3zm16 14H5V6h14v12z"/>
            <path d="M7 9h10v2H7zM7 13h10v2H7z"/>
          </svg>
        </div>
        <h3>Sites Institucionais</h3>
        <p>Desenvolvemos sites modernos, responsivos e otimizados para destacar sua marca.</p>
      </article>

      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#fb6c5c" viewBox="0 0 24 24">
            <path d="M7 18c-1.1 0-2 .9-2 2s.9 2 2 2 2-.9 2-2-.9-2-2-2zm10 0c-1.1 0-2 .9-2 2s.9 2 2 2 2-.9 2-2-.9-2-2-2zM7.16 14.26L7 13h10v2H8.83l-.67-1.74zM17 6H7V4h10v2z"/>
          </svg>
        </div>
        <h3>Lojas Virtuais</h3>
        <p>Crie sua loja online para vender produtos e alcançar clientes em todo o país.</p>
      </article>

      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#004990" viewBox="0 0 24 24">
            <path d="M12 7V3l4 4-4 4V9c-3.31 0-6 2.69-6 6 0 1.13.38 2.17 1 3H5c-1.1 0-2 .9-2 2v1h18v-1c0-1.1-.9-2-2-2h-1c.62-.83 1-1.87 1-3 0-3.31-2.69-6-6-6z"/>
          </svg>
        </div>
        <h3>Consultoria Técnica</h3>
        <p>Orientação especializada para escolher as melhores soluções digitais para seu negócio.</p>
      </article>

      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#fb6c5c" viewBox="0 0 24 24">
            <path d="M21 7v4h-2v5c0 1.1-.9 2-2 2h-5v-2h5v-5H9v-2h12zM3 13v-2H1v6c0 1.1.9 2 2 2h6v-2H3v-4z"/>
          </svg>
        </div>
        <h3>Suporte e Manutenção</h3>
        <p>Garantimos o funcionamento contínuo e atualização do seu site ou sistema.</p>
      </article>

      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#004990" viewBox="0 0 24 24">
            <path d="M19 3H5c-1.1 0-2 .9-2 2v14l7-3 7 3V5c0-1.1-.9-2-2-2z"/>
          </svg>
        </div>
        <h3>Landing Pages</h3>
        <p>Criação de páginas objetivas para campanhas e geração de leads com alta conversão.</p>
      </article>

      <article class="card">
        <div class="icon" aria-hidden="true">
          <svg width="48" height="48" fill="#fb6c5c" viewBox="0 0 24 24">
            <path d="M12 12c2.21 0 4-1.79 4-4S14.21 4 12 4 8 5.79 8 8s1.79 4 4 4zm0 2c-2.67 0-8 1.34-8 4v2h16v-2c0-2.66-5.33-4-8-4z"/>
          </svg>
        </div>
        <h3>Portfólio Pessoal</h3>
        <p>Desenvolvimento de portfólios para profissionais mostrarem seus trabalhos e habilidades.</p>
      </article>
    </div>
  </section>
</template>

<style scoped>
.services-cards {
  background-color: #f9fafb;
  padding: 5rem 2rem;
  /* max-width removido */
  margin: 0 auto;
  color: #1e293b;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
}

.services-cards h2 {
  font-size: 2.75rem;
  font-weight: 700;
  margin-bottom: 4rem;
  color: #004990;
}

.cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 3rem;
  justify-content: center; /* centraliza grid no container */
  padding: 0 1rem; /* espaçamento lateral para telas pequenas */
}

.card {
  background: white;
  border-radius: 16px;
  box-shadow: 0 8px 24px rgba(0,0,0,0.1);
  padding: 2.5rem 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  transition: box-shadow 0.3s ease, transform 0.3s ease;
  cursor: default;
  max-width: 320px; /* limita o tamanho máximo de cada card */
  margin: 0 auto; /* para garantir centralização dos cards */
}

.card:hover {
  box-shadow: 0 16px 40px rgba(0,0,0,0.15);
  transform: translateY(-6px);
}

.icon {
  margin-bottom: 1.5rem;
}

h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #004990;
  margin-bottom: 1rem;
}

p {
  font-size: 1rem;
  line-height: 1.6;
  color: #475569;
  margin: 0;
}

@media (max-width: 768px) {
  .services-cards {
    padding: 3rem 1rem;
  }

  .cards-container {
    grid-template-columns: 1fr;
  }

  .card {
    padding: 2rem 1.5rem;
    max-width: 100%;
  }
}
</style>
