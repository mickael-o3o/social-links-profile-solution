<script setup lang="ts">
const links = ['GitHub ', 'Frontend Mentor ', 'LinkedIn', 'Twitter', 'Instagram']
</script>

<template>
  <main class="p-main">
    <article class="c-profile">
      <header class="c-profile__header">
        <img
          src="/images/avatar-jessica.jpeg"
          alt="a picture of Jessica"
          class="c-profile__image-avatar"
        />
        <div class="c-profile__informations">
          <h1 class="c-profile__user-name">Jessica Randall</h1>
          <p class="c-profile__user-adress">London United Kingdom</p>
        </div>
      </header>

      <p class="c-profile__description">"Front-end developer and avid reader."</p>
      <ul class="c-profile__links-container">
        <li v-for="link in links" class="c-profile__link" :key="link">{{ link }}</li>
      </ul>
    </article>
  </main>
</template>

<style lang="scss">
.p-main {
  color: var(--color-white);
  inline-size: 100%;
  max-inline-size: var(--layout-desktop);
  min-block-size: 100vh;
  margin: 0 auto;
  padding-block-start: 10.85rem;
  padding-inline: 1.5rem;
}

.c-profile {
  background-color: var(--color-grey-800);
  inline-size: 100%;
  max-inline-size: 24rem;
  border-radius: 0.8rem;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2.6rem;
  padding-inline: 2.4rem;
  margin: 0 auto;

  &__header {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1.8rem;
  }

  &__image-avatar {
    inline-size: 5.4rem;
    block-size: 5.4rem;
    border-radius: 100%;
  }

  &__informations {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    text-align: center;
  }

  &__user-name {
    font: {
      size: 1.5rem;
      weight: var(--font-weights-600);
    }
  }

  &__user-adress {
    font: {
      weight: var(--font-weights-700);
    }
    color: var(--color-green);
  }

  &__description {
    margin-block-start: 1.8rem;
    text-align: center;
  }

  &__links-container {
    inline-size: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-block-start: 1.6rem;
  }

  &__link {
    background-color: var(--color-grey-700);
    inline-size: 100%;
    block-size: 2.8rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 0.4rem;
    font : {
      size: var(--font-size-paragraph);
      weight: var(--font-weights-700);
    }
    cursor: pointer;

    &:hover {
      background-color: var(--color-green);
      color: var(--color-grey-900);
    }
  }
}
</style>
