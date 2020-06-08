<template>
  <v-app>
    <Nav/>
    <FloatingBtn/>
    <TutoringContents/>
    <Survey/>
  </v-app>
</template>

<script>
import Survey from '@/components/Survey'
import Nav from '@/components/Nav'
import FloatingBtn from '@/components/FloatingBtn'
import TutoringContents from '@/components/TutoringContents'

export default {
  name: 'app',
  components: {
    Nav, FloatingBtn, TutoringContents, Survey
  }
}
</script>