<script setup>
import Table from './Table.vue'

</script>

<template>
    <div>
        <Button>Show users</Button>
        <Button>Sort A - Z</Button>
        <!-- <p v-for="title in titlesTable" >
            {{title}}
        </p> -->
        <div>
            <Table />
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