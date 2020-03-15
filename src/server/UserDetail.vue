<template>
  <div>
    <p>First Name: {{ switchName() }}</p> <button @click="resetName">Reset</button>
    <p>Last Name: Doe</p>
    <p>Age: 22</p>
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
      return this.name.split('').reverse().join('|');
    },
    resetName(){
      this.name = 'name reset'
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
