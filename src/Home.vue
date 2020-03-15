<template>
  <div>
    <user-detail></user-detail>
    <user-info></user-info>
  </div>
</template>

<script>
import ServerStatus from "./ServerStatus.vue";
import UserInfo from "./server/UserInfo";
import UserDetail from "./server/UserDetail"
export default {
  components: {
    "app-server-status": ServerStatus,
    "user-info": UserInfo,
    "user-detail": UserDetail
  }
};
</script>

<style lang="scss">
</style>
