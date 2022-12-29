<template>
  <footer>

    <article>
        <img src="/icons/envelope.svg" width="24px">
        <p>vicente.real02@gmail.com</p>
    </article>

    <article>
        <img src="/icons/phone.svg" width="24px">
        <p>622 03 55 97</p>
    </article>

  </footer>
</template>

<style lang="sass" scoped>

footer
    display: grid
    padding: 1rem
    gap: 1rem
    @media (min-width: 480px)
        padding: 1rem 4rem
    
    @media (min-width: 520px)
        display: flex
        justify-content: space-around

article
    display: grid
    grid-template-columns: .2fr 1.8fr
    align-items: center
    gap: .5rem

</style>