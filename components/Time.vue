<template>
  <h2>{{ date | localizeTime }}</h2>
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
