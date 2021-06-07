<template>
  <div class="box box--xs appointment">
    <div class="date__box">
      <i class="month">march</i>
      <em class="date">30</em>
    </div>
    <div class="contents">
      <span class="label">약속명</span>
      <div id="name">{{ appointment.name }}</div>
    </div>
    <div class="contents">
      <span class="label">참여자</span>
      <div>
        <span v-for="p in appointment.participants" :key="p">{{ p }}</span>
      </div>
    </div>
    <div class="contents">
      <span class="label">장소</span>
      <div>{{ appointment.location }}</div>
    </div>
    <nuxt-link to="/" class="btn--link btn--link--submit">의견내러 가기</nuxt-link>
  </div>
</template>

<script>
export default {
  props: ['appointment'],
}
</script>

<style></style>
