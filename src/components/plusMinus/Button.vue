<script>
    export default {
    props: ['fontTitile']}

    // console.log();
</script>

<template>
    <button type="button" :class="fontTitile"><slot>{{ fontTitile }}</slot></button>
</template>

<style scoped>
button {
    width: 80px;
    margin: 10px;
}
.red {
  color: red;
}
.blue {
    color: blue;
}
.orange {
    color: orange;
}.yellow {
    color: yellow;
}.pink {
    color: pink;
}.aqua {
    color: aqua;
}
.green {
    color: green;
    background-color: white;
}
</style>