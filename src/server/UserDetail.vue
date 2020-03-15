<template>
  <div>
    <p>First Name: {{name}}</p>
    <p>Last Name: Doe</p>
    <p>Age: 22</p>
  </div>
</template>

<script>
// Vue.use(require('vue-faker'));
export default {
  data() {
    return {
      name: 'John'
    };
  }
};
</script>

<style lang="scss" scoped>
p {
  border-left: 3px solid orange;
  padding-left: 15px;
}
</style>
