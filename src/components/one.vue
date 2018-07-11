<template>
    <div id="one">
        <h1>One 组件</h1>
        <button @click="sendMsg">向同级组件传值</button>
    </div>
</template>

<script>
import bus from '../eventBus';
export default {
    methods: {
        sendMsg(){
            bus.$emit("userDefineEvent","这个组件是One")
        }
    }
}
</script>

<style>

</style>
