<template>
  <div>
    <Time />
    <h1>atomuhr.saarland</h1>
    <div class="links">
      <a class="button" href="https://techmob.show">See who created this</a>
      <a class="button" href="https://github.com/henrystoll/atomuhr.saarland">
        Star us on GitHub
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Time from '~/components/Time.vue'

export default Vue.extend({
  components: { Time },
})
</script>

<style lang="scss">
h1 {
  opacity: 0.9;
  font-weight: normal;
  font-size: 1.2rem;
  margin: 0;
  letter-spacing: 6px;
  @media screen and (max-width: 15rem) {
    font-size: 1rem;
  }
}

.links {
  margin: 4rem 0 0 0;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: space-between;
  align-content: stretch;
  align-items: flex-start;
  @media screen and (max-width: 40rem) {
    flex-direction: column;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-content: stretch;
    align-items: stretch;
  }
}

.button {
  display: inline-block;
  padding: 1rem 1.5rem;
  border-radius: var(--border-radius);
  transition: var(--transition);
  background: var(--color-primary);
  color: var(--color-light);
  text-decoration: none;
  font-weight: bold;
  letter-spacing: 1px;
  border: 2px solid var(--color-primary);
  @media screen and (max-width: 40rem) {
    margin: 0 0 2rem 0;
  }
  &:hover {
    background: var(--color-primary-light);
    color: var(--color-dark);
  }
}
</style>
