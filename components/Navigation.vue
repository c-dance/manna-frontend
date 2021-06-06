<template>
    <div class="gnb">
        <div class="inner inline__wrap l--flex--row jt--space">
        <NuxtLink to="/" class="logo__wrap inline"><Logo/></NuxtLink>
        <div>
            <div class="menu__wrap inline">
                <NuxtLink to="/" class="menu">LIST</NuxtLink>
                <NuxtLink to="/calendar" class="menu">CALENDAR</NuxtLink>
                <NuxtLink to="/register" class="menu">REGISTER</NuxtLink>
            </div>
            <div class="util__wrap inline l--flex--row jt--center">
                <a class="text--s text--s--violet">로그아웃</a>
            </div>
        </div>
        </div>
    </div>
</template>
<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
