<script setup>
import { ref } from 'vue';
import Button from './Button.vue';
import Table from './Table.vue';
import { usersArray } from './listUsers';

const visibleTable = ref(false)
const sort = ref(false)

function isVisible() {
    visibleTable.value = !visibleTable.value;
    console.log(first)
}

function onSort() {
    // console.log('sort: ', sort.value);
    // console.log(usersArray)
    usersArray.sort((a, b) => a['name'].localeCompare(b['name']))
    sort.value = !sort.value;
}
function onReset() {
    usersArray.sort((a, b) => a['id'] - b['id'])
        // console.log(usersArray)
    sort.value = !sort.value;

}
</script>

<template>
    <div>
        <Button @click="isVisible" >{{ visibleTable ? "Hide users" : "Show users" }}</Button>
        <Button @click="onSort" :disabled="sort">Sort A - Z</Button>
        <Button @click="onReset" :disabled="!sort">Reset</Button>
        <div>
            <Table :hidden="!visibleTable" :tableSort="sort"/>
        </div>
    </div>
</template>

<style>
table {

border-collapse: unset;
width: 100%;
}

td, th {
border: 1px solid #dddddd;
/* text-align: left; */
white-space: nowrap;
padding: 8px;
}

tr:nth-child(even) {
background-color: #dddddd;
}
</style>