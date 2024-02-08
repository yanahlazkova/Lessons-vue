<script setup>
import Button from './Button.vue'
import Text from './Text.vue'
import { ref } from 'vue';

    const colorsArray = ['red', 'blue', 'aqua', 'yellow', 'green', 'pink', 'orange'];
    const sizeText = ref(14)
    const showText = ref(false);
    const colorText = ref("black")

    function isShow() {
        showText.value = !showText.value
        // console.log(showText.value);
    }
    function changeSize(event) {
        if (event.target.innerText == '+') {
            sizeText.value+= 2;
        } 
        if (event.target.innerText == '-') {
            sizeText.value-= 2;
        }

        console.log(event.target.innerText);
    }
    function changeColor(color) {
        colorText.value = color;
        console.log(colorText.value);
    }

    
</script>
<template>
    <div>
        <Button @click="changeSize">+</Button>
        <Button @click="changeSize">-</Button>
        <div>
            <Button v-for="color in colorsArray" v-bind:fontTitile='color' @click="changeColor(color)">
                {{color}}
            </Button>
        </div>
        <Button @click="isShow">{{ showText ? "Hide" : "Show" }}</Button>
        <div>
            <p :hidden="!showText" :style="`font-size: ${sizeText}px`" >text</p>
            <Text :hidden="!showText" :sizeText="sizeText" :colorText="colorText" />
        </div>
    </div>
</template>

<style scoped>

</style>