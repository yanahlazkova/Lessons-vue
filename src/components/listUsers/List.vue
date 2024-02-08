<script setup>
    import { usersArray } from './listUsers';

    // получим заголовки таблицы
    const titlesTable = [];
    for (const title in usersArray[0]){
        titlesTable.push(title);
    }

</script>

<template>
    <div>
        <Button>Show users</Button>
        <Button>Sort A - Z</Button>
        <p v-for="title in titlesTable" >
            {{title}}
        </p>
    </div>
</template>