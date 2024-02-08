<script setup>
    import { usersArray } from './listUsers';

    defineProps({
    sort: Boolean
});

// получим заголовки таблицы
const titlesTable = [];
for (const title in usersArray[0]){
    titlesTable.push(title);
    // console.log(title);
}


</script>
<template>
    <table>
        <caption><h2>Table of users</h2></caption>
            <thead>
                <tr>
                    <th v-for="title in titlesTable" :key="title">{{ title }}</th>
                </tr>
            </thead>
            <tr v-for="user of usersArray">
                <td v-for="title in titlesTable">{{ user[title] }}</td>
            </tr>
                    
        </table>
</template>

<style scoped>
table {

border-collapse: unset;
width: 100%;
}

td, th {
border: 1px solid #dddddd;
text-align: left;
white-space: nowrap;
padding: 8px;
}

tr:nth-child(even) {
background-color: #dddddd;
}
</style>