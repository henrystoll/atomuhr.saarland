<template>
  <div class="time">{{ date | localizeTime }}</div>
</template>

<script>
import { format } from 'date-fns'
import { de } from 'date-fns/locale'
export default {
  filters: {
    localizeTime(date) {
      if (!date) return ''
      return format(date, 'ppp', { locale: de })
    },
  },
  data() {
    return {
      interval: null,
      date: new Date(),
    }
  },
  beforeDestroy() {
    clearInterval(this.interval)
  },
  created() {
    this.startInterval()
  },
  methods: {
    startInterval() {
      this.interval = setInterval(() => {
        this.date = new Date()
      }, 500)
    },
  },
}
</script>

<style lang="scss">
.time {
  font-family: 'Roboto Mono', sans-serif;
  font-size: 4rem;
  line-height: 1;
  @media screen and (max-width: 40rem) {
    font-size: 2rem;
  }
}
</style>
