<template>
<div>
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

  <main>
    <div class="form__input">
      <label for="name">Cardholder name</label>
      <input type="text" placeholder="Micheal Scott" v-model="card.name" id="name"/>
    </div>

    <div class="form__input">
      <label for="number">Card number</label>
      <input type="number" placeholder="1234 5678 9123 0000" v-model="card.number" id="number"/>
    </div>

    <div class="form__input">
      <label for="end">Exp. date (mm/yy)</label>
      <input type="text" placeholder="MM" v-model="card.endMonth" id="end"/>
      <input type="text" placeholder="YY" v-model="card.endYear" id="end"/>
    </div>

    <div class="form__input">
      <label for="cvc">CVC</label>
      <input type="number" placeholder="123" v-model="card.backNumber" id="cvc"/>
    </div>

    <div class="form__input">
      <input type="submit" value="Confirm" class="form__input--button">
    </div>
  </main>
 </div>
</template>

<script>
export default {
  data() {
    return {
      card: {
        number: '0000 0000 0000 0000',
        name: 'Micheal Scott',
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
  width: 100%;
  color: white;
  padding-top: 30px;
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
  font-weight: 500;
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
}

main {
  margin-top: 60px;
}

.form__input{
  display: flex;
  flex-direction: column;
  margin: 20px 0px;
}

.form__input label {
  text-transform: uppercase;
  margin-bottom: 5px;
}

.form__input input{
  border: hsl(270, 3%, 87%) solid 1px;
  border-radius: 10px;
  padding: 15px;
  color: hsl(270, 3%, 87%);
  font-family: 'Space Grotesk', sans-serif;
}

.form__input--button{
  background-color: hsl(278, 68%, 11%);
  color: white !important;
  font-size: 1.1rem;
  font-weight: 500;
  border: hsl(278, 68%, 11%) !important;
  margin-top: 10px;
}
</style>
