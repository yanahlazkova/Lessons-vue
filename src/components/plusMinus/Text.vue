<script>
    export default {
    props: ['sizeText', 'colorText']
    }
    console.log("size: I am this");
</script>

<template>
    <div>
        <!-- <p :style="`font-size: ${sizeText}px; color: ${colorText}`"> -->
        <p :style="`font-size: ${sizeText}px`" :class="colorText" >
            <h3>What are Components?</h3><br>
Components are reusable and self-contained pieces of code that encapsulates a specific part of the user interface, 
so that we can make Vue applications that are scalable and easier to maintain.<br>
        We can make components in Vue ourselves, or use built-in components that we will learn about later, like 
            &ltTeleport&gt or &ltKeepAlive&gt. Here we will focus on components we make ourselves.</p>
    </div>
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