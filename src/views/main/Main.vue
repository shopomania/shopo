<template>
    <div>
        <things-table />

    </div>
</template>

<script lang="ts">
import {Component, Vue, Watch} from 'vue-property-decorator';
import ThingsTable from '@/components/things-table/ThingsTable.vue';


@Component({
    components: {
        ThingsTable,
    },
})
export default class Main extends Vue {

}
</script>

<style lang="scss">

</style>