<template>
    <div id="two">
        <h1>One 组件</h1>
        <p>从ONE接受值:{{msg}}</p>
    </div> 
</template>

<script>
import bus from '../eventBus';
export default {
    data () {
        return {
            msg:"默认值"
        }
    },
    mounted () {
        bus.$on("userDefineEvent",(msg)=>{
            this.msg=msg
        })
    }
}
</script>

<style>

</style>
