<template>
    <div class="things-table">
        <thing-item v-for="item in things" :key="item.id" :thing="item">
        </thing-item>

    </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import ThingItem from '@/components/things-table/thing-item/ThingItem.vue';
import things from '@/things/info';

@Component({
    components: {
        ThingItem,
    },
})
export default class ThingsTable extends Vue {
    things = things;

    // public things: any = '';

    public mounted() {
       
        // var rawFile = new XMLHttpRequest();
        // rawFile.open("GET", 'data/2.csv', false); 
        // rawFile.onreadystatechange = () => {
        //     if(rawFile.readyState === 4) {
        //         if(rawFile.status === 200) {
        //             let fileData: any = rawFile.responseText.split('\r\n');
        //             let fileHeader = fileData.splice(0,1)[0].split(',');
        //             fileHeader = fileHeader.reduce((acc: any, element: string, index: number) => {
        //                 return Object.assign(acc, { [element]: index })
        //             }, {});
                   
        //             this.things = fileData.map((element: any) => {
        //                 let temp = element.split(',');
        //                 let obj: any = {};
        //                 for (const key in fileHeader) {
        //                     obj[key]=temp[fileHeader[key]];
        //                 }
        //                 return obj;

        //             });
        //         }
        //     }
        // }
        // rawFile.send(null); 

    }
}
</script>

<style lang="scss">
.things-table {
    margin-left: 400px;
    margin-top: 50px;
    display: flex;
    flex-wrap: wrap;
}
</style>