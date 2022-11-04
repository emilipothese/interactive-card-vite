<template>
<div class="grid">
  <header>
    <section class="card__front">
      <img class="card__front__logo" src="../assets/card-logo.svg" alt="">
      <p v-if="newCard.number" class="card__front__number">{{ newCard.number }}</p>
      <p v-else class="card__front__number">{{ card.number }}</p>
      <div class="card__front__infos">
        <p v-if="newCard.name">{{ newCard.name }}</p>
        <p v-else>{{ card.name }}</p>
        <p>
          <span v-if="newCard.endMonth">{{ newCard.endMonth }}</span>
          <span v-else>{{ card.endMonth }}</span> /
          <span v-if="newCard.endYear">{{ newCard.endYear }}</span>
          <span v-else>{{ card.endYear }}</span>
        </p>
      </div>
    </section>

    <section class="card__back">
      <p v-if="newCard.backNumber" class="card__back__number">{{ newCard.backNumber }}</p>
      <p v-else class="card__back__number">{{ card.backNumber }}</p>
    </section>
  </header>

  <main>
    <div>
      <img src="../assets/icon-complete.svg" alt="">
      <h1>Thank you!</h1>
      <p>We've added your card details</p>
    </div>

    <div class="form__input">
      <input type="submit" value="Continue" class="form__input--button">
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
      },
      newCard: {
        number: '',
        name: '',
        endMonth: '',
        endYear: '',
        backNumber: ''
      }
    };
  },
};
</script>

<style scope>
main {
  text-align: center;
}

h1 {
  text-transform: uppercase;
}

main p {
  color: hsl(279, 6%, 55%)
}
</style>
