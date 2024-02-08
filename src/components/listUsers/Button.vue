<script>
    export default {
    props: ['fontTitile','disabled']}

    // console.log();
</script>

<template>
    <button :disabled="disabled" type="button" :class="fontTitile">
        <slot></slot>
    </button>
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