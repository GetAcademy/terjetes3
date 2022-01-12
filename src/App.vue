<template>
  <div id="app" >
    <div style="display: flex; flex-direction: row">
    <ThingList :things="things" @thing-selected="selectedThing" />
    <ThingDetail :thing="selectedThingObject" />
    </div>
    <div>Valgt ting: {{ selectedThingObject == null ? 'ingenting' : selectedThingObject.name }}</div>
  </div>
</template>

<script>
import ThingList from "./components/ThingList.vue";
import ThingDetail from "./components/ThingDetail.vue";

export default {
  name: "App",
  data() {
    return {
      selectedThingObject: null,
      things: [
        { id: 1, name: "a", value: 123 },
        { id: 2, name: "b", value: 427 },
        { id: 3, name: "c", value: 195 },
      ],
    };
  },
  components: {
    ThingList,
    ThingDetail,
  },
  methods: {
    selectedThing(thing) {
      this.selectedThingObject = thing;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
