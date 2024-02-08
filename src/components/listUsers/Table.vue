<script>
    import { usersArray } from './listUsers';

// получим заголовки таблицы
const titlesTable = [];
for (const title in usersArray[0]){
    titlesTable.push(title);
}
</script>
<template>
        <!-- <p v-for="title in titlesTable" >
            {{title}}
        </p> -->
        <table>
            <caption><h2>Table of users</h2></caption>
                <!-- -- Шапка таблицы --  -->
            <thead>
                <tr v-for="title in titlesTable" >
                    {{title}}
                </tr>
            </thead>
                <!-- Список пользователей -->
                    <!-- {arrayUsers} -->
        </table>
</template>

<style scoped>
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