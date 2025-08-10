<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Pagination, Autoplay } from 'swiper/modules';

import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

const servicos = [
  {
    titulo: "Portfólio Pessoal",
    emoji: "👤",
    descricao:
      "Se apresente ao mundo de uma forma profissional com um portfólio claro, objetivo e visualmente impactante.",
    dicaTitulo: "Dica para seu Portfólio",
    dicaDescricao:
      "Mantenha seu portfólio sempre atualizado, destaque seus melhores projetos e utilize imagens de qualidade.",
    imagem:
      "https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Landing Pages",
    emoji: "📄",
    descricao:
      "Páginas estratégicas focadas em conversão, ideais para captar leads e promover campanhas eficazes.",
    dicaTitulo: "Dica para Landing Pages",
    dicaDescricao:
      "Use chamadas claras e botões de ação para garantir que visitantes convertam facilmente.",
    imagem:
      "https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "E-commerce",
    emoji: "🛒",
    descricao:
      "Soluções completas para lojas online, com sistema de pagamento integrado e gestão eficiente de produtos.",
    dicaTitulo: "Dica para E-commerce",
    dicaDescricao:
      "Invista em uma navegação simples e confiável para melhorar a experiência do usuário e aumentar vendas.",
    imagem:
      "https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Consultoria Digital",
    emoji: "📊",
    descricao:
      "Orientação especializada para melhorar sua presença online e estratégias digitais com foco em resultados.",
    dicaTitulo: "Dica para Consultoria",
    dicaDescricao:
      "Analise dados e feedbacks para ajustar continuamente suas estratégias digitais.",
    imagem:
      "https://images.unsplash.com/photo-1556740738-b6a63e27c4df?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Sites Institucionais",
    emoji: "🏢",
    descricao:
      "Criação de sites profissionais para empresas que desejam fortalecer sua imagem institucional online.",
    dicaTitulo: "Dica para Sites Institucionais",
    dicaDescricao:
      "Mantenha o design limpo e informações claras para transmitir credibilidade aos visitantes.",
    imagem:
      "https://images.unsplash.com/photo-1507679799987-c73779587ccf?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Gestão de Stock",
    emoji: "📦",
    descricao:
      "Sistemas para controle eficiente de estoque, facilitando o gerenciamento e prevenindo perdas.",
    dicaTitulo: "Dica para Gestão de Stock",
    dicaDescricao:
      "Utilize notificações e relatórios para manter seu estoque sempre atualizado e otimizado.",
    imagem:
      "https://images.unsplash.com/photo-1542831371-29b0f74f9713?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Blogs",
    emoji: "✍️",
    descricao:
      "Plataformas para publicação de conteúdo, aumentando sua autoridade e engajamento online.",
    dicaTitulo: "Dica para Blogs",
    dicaDescricao:
      "Produza conteúdo relevante e mantenha uma frequência regular para atrair e fidelizar leitores.",
    imagem:
      "https://images.unsplash.com/photo-1515377905703-c4788e51af15?auto=format&fit=crop&w=600&q=80",
  },
  {
    titulo: "Suporte Técnico",
    emoji: "🛠️",
    descricao:
      "Assistência especializada para resolver problemas técnicos e manter seus sistemas sempre funcionando.",
    dicaTitulo: "Dica para Suporte Técnico",
    dicaDescricao:
      "Ofereça canais de atendimento claros e esteja sempre disponível para atender seus clientes com rapidez.",
    imagem:
      "https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80",
  },
];
</script>

<template>
  <section class="servicos-section">
    <Swiper
      :modules="[Navigation, Pagination, Autoplay]"
      navigation
      pagination
      :autoplay="{ delay: 6000, disableOnInteraction: false }"
      loop
      class="servicos-swiper"
      grab-cursor="true"
    >
      <SwiperSlide v-for="(servico, i) in servicos" :key="i">
        <div class="servico-container">
          <div class="lado-esquerdo">
            <div class="emoji">{{ servico.emoji }}</div>
            <h2>{{ servico.titulo }}</h2>
            <p>{{ servico.descricao }}</p>
          </div>
          <div class="lado-direito">
            <img :src="servico.imagem" :alt="servico.titulo" />
            <div class="dicas">
              <h3>{{ servico.dicaTitulo }}</h3>
              <p>{{ servico.dicaDescricao }}</p>
            </div>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<style scoped>
/* Container da sessão full screen */
.servicos-section {
  width: 100%;
  height: 100vh;
  overflow-x: hidden;
  background: #f4f7fb;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 1rem;
  box-sizing: border-box;
}

/* Swiper geral */
.servicos-swiper {
  width: 90%;
  height: 90vh;
  box-sizing: border-box;
  box-shadow: 0 8px 25px rgb(0 0 0 / 0.15);
  border-radius: 20px;
  overflow: hidden;
}

/* Container do serviço dividido */
.servico-container {
  display: flex;
  height: 100%;
  border-radius: 20px;
  overflow: hidden;
  font-family: 'Segoe UI', sans-serif;
  box-shadow: inset 0 0 50px rgb(0 73 144 / 0.15);
}

/* Lado esquerdo azul navy */
.lado-esquerdo {
  background-color: var(--navy);
  color: white;
  flex: 1;
  padding: 4rem 3rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1.5rem;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
  position: relative;
}

/* Emoji colorido e maior no topo do lado esquerdo */
.emoji {
  font-size: 4.5rem;
  line-height: 1;
  margin-bottom: 1rem;
  filter: drop-shadow(1px 1px 1px rgba(0,0,0,0.2));
  user-select: none;
}

/* Títulos no lado esquerdo */
.lado-esquerdo h2 {
  font-size: 3.2rem;
  margin: 0;
  font-weight: 700;
  letter-spacing: 1.2px;
}

/* Texto do lado esquerdo */
.lado-esquerdo p {
  font-size: 1.3rem;
  line-height: 1.5;
  margin: 0;
}

/* Lado direito branco */
.lado-direito {
  background-color: white;
  flex: 1;
  padding: 3rem 3rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1.5rem;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  box-sizing: border-box;
  color: #222;
}

/* Imagem do lado direito */
.lado-direito img {
  max-width: 100%;
  height: auto;
  max-height: 240px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 6px 20px rgb(0 73 144 / 0.3);
  user-select: none;
  pointer-events: none;
}

/* Dicas no lado direito */
.lado-direito .dicas h3 {
  margin: 0;
  font-weight: 700;
  color: #004990;
  font-size: 1.5rem;
}

.lado-direito .dicas p {
  margin: 0;
  font-size: 1.1rem;
  line-height: 1.5;
}

/* Responsividade */
/* ...existing code... */

/* Responsividade */
@media (max-width: 700px) {
  .servicos-swiper {
    width: 100%;
    height: 97vh;
  }

  .servico-container {
    flex-direction: column;
    height: 97vh;
  }

  .lado-esquerdo,
  .lado-direito {
    padding: 1rem 2rem;
    box-sizing: border-box;
  }

  .lado-esquerdo {
    height: 45vh;
    border-bottom-left-radius: 0;
  }

  .lado-direito {
    height: 55vh;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    color: #222;
    width: 100%;
    padding-left: 0;
    padding-right: 0;
    padding-top: 0;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
    border-top-right-radius: 0;
    border-top-left-radius: 0;
  }

  .lado-direito img {
    width: 100%;
    height: 190px; /* imagem maior */
    object-fit: cover;
    border-radius: 0;
    box-shadow: 0 6px 20px rgb(0 73 144 / 0.3);
    margin-top: 0 !important; /* garante que não há espaço superior */
    align-self: center;
    display: block;
  }

  .lado-direito .dicas {
    margin: 0 1rem 0 1rem; /* menos espaço inferior */
  }

  .lado-esquerdo h2 {
    font-size: 1.5rem;
  }

  .lado-direito .dicas h3 {
    font-size: 1rem;
  }

  .emoji {
    font-size: 2rem;
    margin-bottom: 0.5rem;
  }
}
</style>
