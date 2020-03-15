<template>
  <div>
    <div class="card">
      <button @click="changeName">Change Name</button>
    <user-detail :name="name"></user-detail>
    <user-detail></user-detail>
    <user-info></user-info>
    </div>
  </div>
</template>

<script>
import ServerStatus from "./ServerStatus.vue";
import UserInfo from "./server/UserInfo";
import UserDetail from "./server/UserDetail"
export default {
  data (){
    return{
      name: 'John',
    }
  },
  methods: {
    changeName (){
      this.name = 'changed name';
    }

  },
  components: {
    "app-server-status": ServerStatus,
    "user-info": UserInfo,
    "user-detail": UserDetail
  }
};
</script>

<style lang="scss">
</style>
