<template>
  <div>
    <div class="jumbotron">
      <p>The Name is:  {{name}}</p>
      <button @click="changeName">Change Name</button>
      <div class="row">
        <div class="col-sm-6">
          <user-detail :name="name" @nameWasReset="name = $event "></user-detail>
        </div>
        <div class="col-sm-6 d-none">
          <user-detail></user-detail>
        </div>
      <div class="col-sm-6">
      <user-info></user-info>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
import ServerStatus from "./ServerStatus.vue";
import UserInfo from "./server/UserInfo";
import UserDetail from "./server/UserDetail";
export default {
  data() {
    return {
      name: "John"
    };
  },
  methods: {
    changeName() {
      this.name = "changed name";
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
