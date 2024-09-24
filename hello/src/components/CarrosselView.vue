<template>
  <div class="carrossel">
    <swiper
      :modules="modules"
      :slides-per-view="1"
      :space-between="50"
      navigation
      :pagination="{ clickable: true }"
      :autoplay="{ delay: 3000, disableOnInteraction: false }"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide v-for="slide in slides" :key="slide.id">
        <div class="slide-content">
          <h2>{{ slide.titulo }}</h2>
          <p>{{ slide.descricao }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination, Autoplay } from "swiper/modules";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

export default {
  name: "CarrosselView",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      modules: [Navigation, Pagination, Autoplay],
      slides: [
        {
          id: 1,
          titulo: "Bem-vindo ao Petshop",
          descricao: "Cuidamos do seu melhor amigo com amor",
        },
        {
          id: 2,
          titulo: "Promoção de Rações",
          descricao: "Até 30% de desconto em rações premium",
        },
        {
          id: 3,
          titulo: "Serviço de Banho e Tosa",
          descricao: "Agende agora e ganhe 10% de desconto",
        },
      ],
    };
  },
  methods: {
    onSwiper(swiper) {
      console.log(swiper);
    },
    onSlideChange() {
      console.log("slide change");
    },
  },
};
</script>

<style scoped>
.carrossel {
  margin-bottom: 2rem;
}

.swiper {
  width: 100%;
  height: 400px; /* Ajuste conforme necessário */
}

.swiper-slide {
  position: relative;
}

.swiper-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.slide-content {
  position: absolute;
  bottom: 20px;
  left: 20px;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.slide-content h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.slide-content p {
  font-size: 16px;
}
</style>
