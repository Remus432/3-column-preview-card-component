<script>
  export let carIcon
  export let carType
  export let carDescription
  export let color
  export let index
</script>

<div style="background-color: {color}" class="card card--{index+1}">
  <img src={carIcon} alt="Car Icon" class="card__icon">
  <h2 class="card__headline">{carType}</h2>
  <p class="card__description">{carDescription}</p>
  <button style="color: {color}" class="card__btn">Learn More</button>
</div>

<style lang="scss">
  .card {
    padding: 4.8rem;

    &:first-of-type {
      border-top-left-radius: .8rem;
      border-top-right-radius: .8rem;
    }

    &:last-of-type {
      border-bottom-left-radius: .8rem;
      border-bottom-right-radius: .8rem;
    }

    & > *:first-child { 
      margin-bottom: 3.5rem;
    }

    & > *:not(:first-child) {
      margin-bottom: 2.5rem;
    }

    &__headline {
      color: hsl(0, 0%, 95%);
      font-family: "Big Shoulders Display";
      font-size: 4rem;
      text-transform: uppercase;
    }

    &__description {
      color: hsla(0, 0%, 100%, 0.75);
    }

    &__btn {
      background-color: hsl(0, 0%, 95%);
      border: 2px solid transparent;
      border-radius: 2.5rem;
      font-family: "Lexend Deca";
      padding: 1.1rem 3.15rem;
    }

    @media screen and (min-width: 768px) {
      &--1 {
        animation: fadeInDown 1s backwards ease-in-out;
      }

      &--2 {
        animation: fadeInDown 1s .5s backwards ease-in-out;
      }

      &--3 {
        animation: fadeInDown 1s 1s backwards ease-in-out;
      }

      &:first-of-type {
        border-radius: unset;
        border-top-left-radius: .8rem;
        border-bottom-left-radius: .8rem;
      }

      &:last-of-type {
        border-radius: unset;
        border-top-right-radius: .8rem;
        border-bottom-right-radius: .8rem;
      }

      &__btn {
        cursor: pointer;

        &:hover {
          background-color: transparent;
          border: 2px solid hsl(0, 0%, 95%);
          color: hsl(0, 0%, 95%)!important;
        }
      }
    }
  }
</style>