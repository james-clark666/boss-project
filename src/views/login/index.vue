<template>
  <div class="login">用户登录</div>
</template>

<script lang="ts">
import Vue from 'vue'
import request from '@/utils/request'
export default Vue.extend({
  name: 'LoginIndex',
  data () {
    return {}
  },
  methods: {
    async onSubmit () {
      const { data } = await request({
        method: 'POST',
        url: '/front/user/login'
      })
      console.log(data)
    }

  }
})
</script>

<style lang="scss" scoped></style>
