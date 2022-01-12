
<template>
  <div >
    <h3>ThingDetail</h3>
    Navn: {{thing.name}}<br/>
    Value: {{thing.value}}<br/>
    Id: {{thing.id}}<br/>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  props: ['thing'],
  components: {
    // HelloWorld,
  },
};
</script>

<style>
</style>
