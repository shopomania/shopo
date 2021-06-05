<template>
  <v-app>
    <things-table />
  </v-app>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import ThingsTable from '@/components/things-table/ThingsTable.vue';


@Component({
    components: {
        ThingsTable,
    },
})
export default class App extends Vue {

}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>

<style lang="scss" src="@/assets/styles/app.scss"></style>




