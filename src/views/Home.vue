<template>
  <div class="chronology">
    <Header />
    <Section />
    <Footer />
  </div>
</template>

<script>

import Header from '@/components/Header'
import Section from '@/components/Section'
import Footer from '@/components/Footer'

export default {
  name: 'Home',
  components: {
    Header,
    Section,
    Footer
  }
}
</script>
<style lang="scss" scoped>

</style>