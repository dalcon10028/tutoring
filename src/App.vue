<template>
  <v-app>
    <Nav/>
    <FloatingBtn/>
    <TutoringContents/>
  </v-app>
</template>

<script>
import Nav from '@/components/Nav'
import FloatingBtn from '@/components/FloatingBtn'
import TutoringContents from '@/components/TutoringContents'

export default {
  name: 'app',
  components: {
    Nav, FloatingBtn, TutoringContents
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Jua&family=Nanum+Brush+Script&family=Nanum+Gothic&family=Noto+Sans+KR:wght@400;700&display=swap');
</style>