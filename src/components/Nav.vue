<template>
  <v-navigation-drawer
    v-model="drawer"
    app
  >
  <v-row class="fill-height" align="center" justify="center">
    <v-list flat rounded>
      <v-list-item-group color="primary">
        <!-- 홈 -->
        <v-list-item link v-for="(item, idx) in menu" v-bind:key="idx" @click="MoveMenu(idx)">
          <v-list-item-content>
            <v-list-item-title class="nav-item">{{item}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <v-btn
      small
      absolute
      fixed
      outlined color="indigo"
      bottom
      @click="ChangeDarkTheme"
    >
    <v-icon small>mdi-lightbulb-on-outline</v-icon>
    {{theme.text}}
    </v-btn>
    </v-row>
  </v-navigation-drawer>
</template>

<script>
  export default {
    props: {
      source: String,
    },
    data(){
      return{
        drawer : true,
        menu : ['홈', '동반성장 튜터링이란?', 'CodeRunner 소개', '튜터소개', '신청서 작성'],
        theme : {
          text : '다크모드',
        }
      }
    },
    methods: {
      MoveMenu : function(idx){
        let move;
        switch (idx) {
          case 0: move='#home'; break;
          case 1: move='#about'; break;
          case 2: move='#coderunner'; break;
          case 3: move='#tutor'; break;
          case 4: move='#survey'; break;
        }
        this.$vuetify.goTo(move);
      },
      ChangeDarkTheme : function() {
        this.$vuetify.theme.dark = !this.$vuetify.theme.dark
        if(this.theme.text === '다크모드') this.theme.text = '라이트모드'
        else this.theme.text = '다크모드'
      }
    }
  }
</script>
<style scoped>
.nav-item{
  font-family: 'Noto Sans KR';
}
</style>