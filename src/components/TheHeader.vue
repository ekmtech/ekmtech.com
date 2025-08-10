<template>
  <header>
    <nav aria-label="Menu principal">
      <ul class="button-container">
        <!-- Logo dentro de <li> para semântica correta -->
        <li class="logo-item">
          <a href="#" aria-label="Página Inicial" class="button logo-button">
            <img src="/src/imgs/EKM tech Logo.png" alt="logo da EKM Tech" class="logo" />
          </a>
        </li>
        <li>
          <a href="#" aria-label="Página Inicial" class="button" title="Página Inicial">
            <i class="fas fa-home icon" aria-hidden="true"></i>
          </a>
        </li>
        <li>
          <a href="#" aria-label="Sobre" class="button" title="Sobre">
            <i class="fas fa-info-circle icon" aria-hidden="true"></i>
          </a>
        </li>
        <li>
          <a href="#" aria-label="Serviços" class="button" title="Serviços">
            <i class="fas fa-briefcase icon" aria-hidden="true"></i>
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  position: fixed;
  top: 15px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1000;

  background-color: rgba(255 255 255 / 0.85);
  border-radius: 40px;
  box-shadow:
    rgba(0 0 0 / 0.35) 0px 5px 15px,
    rgba(0 73 144 / 0.5) 5px 10px 15px;
  
  padding: 15px 30px;
  display: flex;
  justify-content: center;
  width: 70%;
  max-width: 700px;

  /* para suavizar aparecimento */
  backdrop-filter: saturate(180%) blur(10px);
  -webkit-backdrop-filter: saturate(180%) blur(10px);
}

.button-container {
  list-style: none;
  display: flex;
  gap: 2.5rem;
  align-items: center;
  margin: 0;
  padding: 0;
  width: 100%;
  justify-content: center;
}

li {
  position: relative;
}

/* Botões redondos */
.button {
  all: unset;
  cursor: pointer;
  width: 44px;
  height: 44px;
  border-radius: 50%;
  color: #004990;
  font-size: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  z-index: 1;
  user-select: none;
  transition: color 0.3s ease, background-color 0.3s ease;
}

/* Logo com tamanho maior e sem efeito hover */
.logo-button {
  width: auto;
  height: auto;
  cursor: pointer;
}

.logo {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: block;
  object-fit: cover;
}

/* Efeito “abertura” atrás do botão ao passar o mouse */
li::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 54px;
  height: 54px;
  background: #fb6c5c; /* cor coral EKM Tech */
  border-radius: 50%;
  transform: translate(-50%, -50%) scale(0);
  transition: transform 0.4s ease;
  z-index: 0;
}

li:hover::before,
li:focus-within::before {
  transform: translate(-50%, -50%) scale(1);
}

/* Muda cor do ícone no hover/focus para branco */
.button:hover,
.button:focus {
  color: white;
  outline: none;
}

/* Ícones */
.icon {
  pointer-events: none; /* para não atrapalhar clique */
}

/* Responsividade */
@media (max-width: 600px) {
  header {
    width: 90%;
    padding: 12px 20px;
  }

  .button-container {
    gap: 1.8rem;
  }

  .button {
    width: 40px;
    height: 40px;
    font-size: 1.3rem;
  }

  .logo {
    width: 36px;
    height: 36px;
  }
}
</style>
