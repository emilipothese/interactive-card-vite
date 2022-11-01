<template>
  <header>
    <section class="card__front">
      <img class="card__front__logo" src="../assets/card-logo.svg" alt="">
      <p class="card__front__number">{{ card.number }}</p>
      <div class="card__front__infos">
        <p>{{ card.name }}</p>
        <p>{{ card.endMonth }} / {{ card.endYear }}</p>
      </div>
    </section>

    <section class="card__back">
      <p class="card__back__number">{{ card.backNumber }}</p>
    </section>
  </header>
</template>

<script>
export default {
  data() {
    return {
      card: {
        number: '0000 0000 0000 0000',
        name: 'Jane Appleseed',
        endMonth: '00',
        endYear: '00',
        backNumber: '000'
      }
    };
  },
};
</script>

<style scoped>
header {
  background-image: url('../assets/bg-main-desktop.png');
  background-size: cover;

}

.card__front {
  background-image: url('../assets/bg-card-front.png');
  background-size: contain;
  background-repeat: no-repeat;
}

.card__front__logo{
  width: 60px;
}

.card__front__number {
  margin: 30px 0px 0px 0px;
  font-size: 1.3rem;
  font-weight: 800;
}

.card__front__infos {
  display: flex;
  justify-content: space-between;
  text-transform: uppercase;
}

.card__front__infos p {
  margin-bottom: 0px;
  font-size: 0.8rem;
}

.card__back {
  background-image: url('../assets/bg-card-back.png');
  background-size: contain;
  background-repeat: no-repeat;
  padding: 20px 30px;
}
</style>
