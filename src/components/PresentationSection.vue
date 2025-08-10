<script setup>
import TheHeader from './TheHeader.vue';
</script>

<template>
  <TheHeader />

  <main class="page">
    <section class="branding">
      <div class="logo">⧉</div>
      <h1>Otimize sua marca com um site</h1>
      <div class="info">
        <p>EKM Tech</p>
        <span>Desenvolvedores de Software</span>
      </div>

      <p class="description">
        Criamos soluções digitais para impulsionar seu negócio online.
      </p>

      <button class="cta">Trabalhe comigo</button>
    </section>

    <section class="visual">
      <img src="/src/imgs/meninasComCelular.png" alt="Foto representando consultoria" />
      <div class="overlay"></div>
    </section>
  </main>
</template>

<style scoped>
.page {
  display: flex;
  height: 100vh;
  overflow: hidden;
  background: var(--navy);
  color: var(--white);
  font-family: var(--font-primary);
}

.branding,
.visual {
  width: 50%;
  flex-shrink: 0;
  position: relative;
}

.branding {
  background: var(--white);
  color: var(--ekmtechcolor-dark);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 4rem 5rem;
  box-sizing: border-box;
  gap: 1.5rem;
  box-shadow: inset -10px 0 30px -15px var(--navy);
}

.logo {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: var(--coral);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--white);
  user-select: none;
  box-shadow: 0 4px 10px rgba(251,108,92,0.6);
  transition: transform 0.3s ease;
}
.logo:hover {
  transform: scale(1.1);
}

.branding h1 {
  font-size: 3.2rem;
  margin: 0;
  line-height: 1.15;
  font-weight: 800;
}

.info p {
  font-size: 1.3rem;
  margin: 0;
  font-weight: 600;
  letter-spacing: 0.05em;
  color: var(--ekmtechcolor);
}

.info span {
  font-size: 1rem;
  color: var(--ekmtechcolor-dark);
  font-weight: 500;
}

.description {
  font-size: 1.3rem;
  color: var(--ekmtechcolor);
  max-width: 450px;
  line-height: 1.5;
  margin-top: 1rem;
  font-weight: 500;
}

.cta {
  background: var(--ekmtechcolor);
  color: var(--white);
  padding: 1.1rem 3rem;
  border-radius: 16px;
  font-weight: 700;
  margin-top: 3rem;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
  box-shadow: 0 8px 20px rgba(0, 73, 144, 0.45);
  align-self: start;
  user-select: none;
}
.cta:hover {
  background: var(--ekmtechcolor-dark);
  transform: translateY(-3px);
  box-shadow: 0 14px 28px rgba(0, 58, 120, 0.55);
}

.visual {
  flex: 1;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}
.visual img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  user-select: none;
  pointer-events: none;
  filter: brightness(0.75);
  transition: filter 0.4s ease;
}
.visual:hover img {
  filter: brightness(0.85);
}

.visual .overlay {
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: linear-gradient(to left, transparent 0%, var(--navy) 70%);
  pointer-events: none;
}

@media screen and (max-width: 768px) {
  .page {
    flex-direction: column;
    height: auto;
  }

  .branding,
  .visual {
    width: 100%;
    flex: none;
    height: auto;
  }

  .branding {
    padding: 3rem 2rem;
    align-items: center;
    text-align: center;
    gap: 1rem;
    box-shadow: none;
  }

  .logo {
    width: 56px;
    height: 56px;
    font-size: 2rem;
  }

  .branding h1 {
    font-size: 2.2rem;
  }

  .info p,
  .info span {
    font-size: 1.1rem;
  }

  .description {
    max-width: 100%;
    font-size: 1.15rem;
  }

  .cta {
    margin: 2rem auto 0 auto;
    align-self: center;
    padding: 1rem 3.5rem;
  }

  .visual {
    height: 300px;
  }
}
</style>
