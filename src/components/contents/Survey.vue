<template>
  <v-container>
      <v-form
          ref="form"
          v-model="valid">
        <v-text-field
          v-model="name"
          :counter="5"
          :rules="nameRules"
          label="이름"
          required
        ></v-text-field>
        <v-text-field
          v-model="phone"
          :rules="phoneRules"
          label="핸드폰 번호"
          required
        ></v-text-field>

        <v-btn
          :disabled="!valid"
          color="success"
          class="mr-4"
          @click="validate">
          제출하기
        </v-btn>
        <v-btn
          color="error"
          class="mr-4"
          @click="reset">
          초기화
        </v-btn>
        <v-btn
          color="primary"
          class="mr-4"
          @click="save">
          임시저장
        </v-btn>
      </v-form>
  </v-container>
</template>

<script>

export default {
  name: 'Survey',

  data(){
    return{
      valid: true,
      name : '',
      nameRules: [
        v => !!v || '이름을 입력해주세요',
        v => (v && v.length <= 5) || '이름은 5자 이하입니다.',
        v => /^[가-힣]+$/.test(v) || '정확한 이름을 입력해주세요.',
      ],
      phone : '',
      phoneRules: [
        v => !!v || '전화번호를 적어주세요',
        v => /^\d{3}-\d{3,4}-\d{4}$/.test(v) || '유효하지 않은 번호입니다.',
      ],
    }
  },
  methods: {
    validate () {
      this.$refs.form.validate()
    },
    reset () {
      this.$refs.form.reset()
    },
    save(){

    }
  }
};
</script>
