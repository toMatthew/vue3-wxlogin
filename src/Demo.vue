<template>
        <wxlogin :appid="appid" :scope="scope" :redirect_uri="redirect_uri"></wxlogin>

</template>

<script>
import wxlogin from './components/vue-next-wxlogin'
import { reactive, toRefs } from 'vue'

export default {
  name: 'App',
  components: {
    wxlogin
  },
  setup () {
    const state = reactive({
      appid : 'wxe1f5def243e0390b',
      scope : 'snsapi_login',
      redirect_uri : 'https://abstest.tenpay.com/abs/author/callBack.do',
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>

<style>

</style>
