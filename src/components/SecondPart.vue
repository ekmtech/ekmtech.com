<template>
  <section class="why-site-simple">
    <h2>Por que ter um site profissional?</h2>
    <ul class="benefits-list">
      <li>
        <span class="icon" aria-hidden="true">✅</span>
        <div>
          <h3>Credibilidade</h3>
          <p>Construa confiança com clientes mostrando profissionalismo online.</p>
        </div>
      </li>
      <li>
        <span class="icon" aria-hidden="true">🌐</span>
        <div>
          <h3>Presença 24/7</h3>
          <p>Seu negócio disponível a qualquer hora, para qualquer pessoa, em qualquer lugar.</p>
        </div>
      </li>
      <li>
        <span class="icon" aria-hidden="true">🚀</span>
        <div>
          <h3>Expansão</h3>
          <p>Alcance novos mercados e aumente seu público facilmente.</p>
        </div>
      </li>
      <li>
        <span class="icon" aria-hidden="true">🎨</span>
        <div>
          <h3>Controle</h3>
          <p>Personalize a imagem da sua marca do jeito que quiser.</p>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.why-site-simple {
  background-color: var(--navy);
  color: #ffffff;
  padding: 4rem 2rem;
  /* max-width removido */
  margin: 0 auto;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
  max-width: none;
  width: 100%;
  box-sizing: border-box;
}

.why-site-simple h2 {
  font-size: 2.8rem;
  font-weight: 700;
  margin-bottom: 3rem;
  color: #fb6c5c;
}

.benefits-list {
  list-style: none;
  padding: 0 1rem;
  margin: 0 auto;
  text-align: left;
  max-width: 900px;
}

.benefits-list li {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  margin-bottom: 2.5rem;
}

.icon {
  font-size: 3rem;
  color: #fb6c5c;
  flex-shrink: 0;
  line-height: 1;
  margin-top: 6px;
}

.benefits-list h3 {
  margin: 0 0 0.5rem 0;
  font-size: 1.5rem;
  color: #ffffff;
}

.benefits-list p {
  margin: 0;
  font-size: 1.1rem;
  color: #d0d9f0;
  line-height: 1.5;
}

@media (max-width: 768px) {
  .benefits-list li {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .icon {
    margin-top: 0;
  }
}
</style>
