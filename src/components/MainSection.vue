<script setup lang="ts">
const links = ['GitHub ', 'Frontend Mentor ', 'LinkedIn', 'Twitter', 'Instagram']
</script>

<template>
  <main class="profile-container">
    <div class="profile">
      <img src="/images/avatar-jessica.jpeg" alt="avatar jessica" class="image-avatar" />
      <div class="information">
        <h1 class="name">Jessica Randall</h1>
        <p class="adress">London United Kingdom</p>
      </div>
      <p class="description">"Front-end developer and avid reader."</p>
      <ul class="links-container">
        <li v-for="link in links" class="link" :key="link">{{ link }}</li>
      </ul>
    </div>
  </main>
</template>

<style lang="scss">
.profile-container {
  background-color: var(--color-grey-900);
  color: var(--color-white);
  width: 100%;
  max-width: var(--layout-mobile);
  height: 100vh;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;

  @media (min-width: 23.43rem) {
    max-width: var(--layout-desktop);
  }
}

.profile {
  background-color: var(--color-grey-800);
  width: 100%;
  max-width: calc(var(--layout-mobile) - 1rem);
  border-radius: 0.8rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2.2rem;
  gap: 1.5rem;

  .image-avatar {
    width: 5.4remrem;
    height: 5.4rem;
    border-radius: 100%;
  }

  .information {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;

    .name {
      font: {
        size: 1.5rem;
        weight: var(--font-weights-600);
      }
    }

    .adress {
      font: {
        weight: var(--font-weights-700);
      }
      color: var(--color-green);
    }
  }

  .links-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 0.9rem;

    .link {
      background-color: var(--color-grey-700);
      width: 100%;
      height: 2.7rem;
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
}
</style>
