<template>
  <div class="container">
    <div class="box box--xl">
    <h2 class="heading--title">약속 캘린더</h2>
    <div class="l--flex--row jt--space pd--l">
        <!-- 캘린더 -->
        <div class="calendar l--table">
          <div class="l--cell">
          <no-ssr>
            <v-date-picker
              is-expanded
              v-model="pickdate"
              :attributes="attrs"
              :model-config="modelConfig"
              is-required
            />
          </no-ssr>
          </div>
        </div>
        <!-- 날짜별 일정-->
        <div>
          <schedule :date="pickdate" />
        </div>
    </div>
    <!-- submit -->
    <div class="text--center">
      <nuxt-link
        to="/register"
        class="btn--submit btn--submit--m mg--m"
        :date="pickdate"
      >
        이 날 약속 추가하기
      </nuxt-link>
    </div>
    </div>
  </div>
</template>

<script>
import Schedule from '~/components/Calendar/Schedule.vue'

export default {
  components: {
    Schedule,
  },
  data() {
    return {
      isShow: false,
      attrs: [
        {
          key: 'today',
          bar: 'red',
          dates: new Date(2021, 6, 15),
        },
      ],
      start: '',
      type: 'month',
      pickdate: new Date(2021, 6, 5), // yyyy-mm-dd 형식으로 바꾸는법은?
      modelConfig: {
        type: 'string',
        mask: 'YYYY-MM-DD',
      },
    }
  },
}
</script>
