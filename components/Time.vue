<template>
  <h2>{{ date | localizeTime }}</h2>
</template>

<script>
import { format } from 'date-fns'
export default {
  filters: {
    localizeTime(date) {
      if (!date) return ''
      return format(date, 'ppp')
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
<style>
.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>
