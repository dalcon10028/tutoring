<template>
    <a href="http://pf.kakao.com/_RqjcT/chat" target="_blank" rel="noopener noreferrer">
    <v-btn
        absolute
        fab
        fixed
        small
        dark
        rounded
        bottom
        right
        color="pink"
    >
    <v-icon small>mdi-chat</v-icon>카톡으로 문의하기
    </v-btn>
    </a>
</template>
<script>
export default {
    name: 'FloatingBtn',
    methods : {
    }
}
</script>
<style scoped>
/* 버튼 위치 조정 */
.v-btn--fab.v-size--small.v-btn--absolute.v-btn--bottom{
    bottom: 1rem;
}
/* 버튼 크기 조정 */
.v-btn--fab.v-size--small{
    width: 9rem;
    height: 2rem;
}
</style>