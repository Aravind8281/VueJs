<template>
  <div>
    <h2>Component Lifecycle Example</h2>
    <p>Current Message: {{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello, Vue!'
    };
  },
  beforeCreate() {
    console.log('beforeCreate: Component is about to be created.');
  },
  created() {
    console.log('created: Component has been created.');
  },
  beforeMount() {
    console.log('beforeMount: Component is about to be mounted to the DOM.');
  },
  mounted() {
    console.log('mounted: Component has been mounted to the DOM.');
  },
  beforeUpdate() {
    console.log('beforeUpdate: Component is about to be updated.');
  },
  updated() {
    console.log('updated: Component has been updated.');
  },
  beforeDestroy() {
    console.log('beforeDestroy: Component is about to be destroyed.');
  },
  destroyed() {
    console.log('destroyed: Component has been destroyed.');
  },
  methods: {
    changeMessage() {
      this.message = 'Vue is awesome!';
    }
  }
};
</script>

<style scoped>
/* Your styles go here */
</style>
