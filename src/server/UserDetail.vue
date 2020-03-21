<template>
  <div class="jumbotron bg-info">
    <p>First Name: {{ switchName() }}</p>
    <p>Last Name: Doe</p>
    <p>Age: 22</p>
    <button @click="resetName">Reset</button>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      // required: true,
      default: 'Max',
    }
  },
  methods: {
    switchName(){
      // return this.name.split('').reverse().join('|');
      return this.name.split('').join('|');
    },
    resetName(){
      this.name = 'name reset';
      this.$emit('nameWasReset', this.name);
      }
  }
};
</script>

<style lang="scss" scoped>
p {
  border-left: 3px solid orange;
  padding-left: 15px;
}
</style>
