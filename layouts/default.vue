<template>
  <div>
    <main>
      <Nuxt />
    </main>
  </div>
</template>

<style lang="scss">
:root {
  --color-primary: #ff9f61;
  --color-primary-light: #ffecdf;
  --color-dark: #332013;
  --color-light: #fff;
  --color-gradient: radial-gradient(
    129.55% 129.55% at 6.6% 2.7%,
    #ffe897 0%,
    #ff4820 100%
  );
  --transition: all 0.15s ease-in-out;
  --border-radius: 0.25rem;
}

html {
  font-family: Open Sans, Helvetica Neue, Arial, sans-serif;
  font-size: 16px;
  box-sizing: border-box;
  color: var(--color-dark);
  line-height: 1.75;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background: radial-gradient(
    129.55% 129.55% at 6.6% 2.7%,
    rgba(255, 232, 151, 0.3) 0%,
    rgba(255, 72, 32, 0.3) 100%
  );
}

main {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  @media screen and (max-width: 40rem) {
    width: calc(100% - 4rem);
    margin: 2rem;
  }
}
</style>
