<template>
  <div class="amenities-section">
    <h2 class="section-title">AMENIDADES Y SERVICIOS COMPLEMENTARIOS</h2>
    <div class="grid">
      <div class="card" v-for="(item, index) in amenities" :key="index">
        <div class="icon">{{ item.icon }}</div>
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      amenities: [
        { icon: "🏋️", title: "JAZZERCISE Pedregal", description: "Atención personalizada" },
        { icon: "🎾", title: "Padel ON", description: "Reservación previa" },
        { icon: "💆‍♀️", title: "Estética", description: "Servicio integral" },
        { icon: "🍽️", title: "HALOCLINA CATERING", description: "Atención personalizada" },
        { icon: "🧘", title: "INNATE", description: "Reservación previa" },
        { icon: "🥋", title: "The Jab", description: "Servicio integral" },
      ],
    };
  },
};
</script>

<style scoped>
.amenities-section {
  background-color: #1a1d1d;
  color: white;
  text-align: center;
  padding: 60px 20px;
  font-family: 'Helvetica Neue', sans-serif;
}

.section-title {
  font-size: 22px;
  font-weight: bold;
  margin-bottom: 40px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(260px, 1fr));
  gap: 20px;
  max-width: 1100px;
  margin: 0 auto;
}

.card {
  background-color: #111314;
  border: 1px solid #333;
  border-radius: 8px;
  padding: 20px;
  text-align: left;
}

.icon {
  font-size: 20px;
  color: #f37021;
  margin-bottom: 10px;
}

.card h3 {
  font-size: 16px;
  font-weight: bold;
  margin: 0 0 5px;
}

.card p {
  font-size: 14px;
  color: #ccc;
}

</style>
