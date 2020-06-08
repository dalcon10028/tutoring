<template>
  <v-container>
    <v-content>
      <section id="home">
        <Home/>
      </section>
      <section id="about">
        <h1 class="font-weight-black">동반성장 튜터링이란?</h1>
      </section>
      <section id="coderunner">
        <h1>CodeRunner 소개</h1>
      </section>
      <section id="tutor">
        <h1>튜터 소개</h1>
      </section>
      <section id="survey">
        <h1>신청서 작성</h1>
      </section>
    </v-content>
  </v-container>
</template>
<script>
import Home from '@/components/contents/Home'

export default {
  name: 'TutoringContents',
  components: {
    Home
  }
}

</script>
<style scoped>
section{
  margin-top: 5rem;
}
</style>