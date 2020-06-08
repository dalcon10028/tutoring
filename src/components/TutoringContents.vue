<template>
  <v-container>
    <v-content>
      <section id="home">
        <Home/>
      </section>
      <section id="about">
        <About/>
      </section>
      <section id="coderunner">
        <CodeRunner/>
      </section>
      <section id="tutor">
        <Tutor/>
      </section>
      <section id="survey">
        <Survey/>
      </section>
    </v-content>
  </v-container>
</template>
<script>
import Home from '@/components/contents/Home'
import About from '@/components/contents/About'
import CodeRunner from '@/components/contents/CodeRunner'
import Tutor from '@/components/contents/Tutor'
import Survey from '@/components/contents/Survey'

export default {
  name: 'TutoringContents',
  components: {
    Home, About, CodeRunner, Tutor, Survey
  }
}

</script>
<style scoped>
section{
  margin-top: 5rem;
}
</style>