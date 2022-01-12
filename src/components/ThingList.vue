<template>
  <div >
    <h3>ThingList</h3>
    {{status}}
    <ul v-for="thing in things" v-bind:key="thing.id">
      <li>
        {{thing.name}} {{thing.value}}
        <button @click="selectThing(thing)">velg</button>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: "App",
  data(){
    return {status: 'ingenting valgt'}
  },
  props: ['things'],
  methods:{
    selectThing(thing){
      this.status = `${thing.name} er valgt`;
      this.$emit('thing-selected', thing);
    }
  }
};
</script>

<style>
</style>
