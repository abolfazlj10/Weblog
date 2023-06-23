<script>
import Heading from './heading.vue';
export default{
    props: ["head"],
    components: { Heading },
    data(){
        return{
            show:true
        }
    }
}
</script>
<template>
    <div class="BS">
        <div @click="" class="TS">
            <div class="fontIcon IM">&#xf077;</div>
            <Heading :txt="head" type="side"/>
        </div>
        <slot></slot>    
    </div>
</template>
<style scoped>
.BS{ /* Box Side */
    background-color: #FFF;
    padding:10px 20px;
    border-radius: 10px;
}
.TS{ /* Top Section */
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-between;
    cursor: pointer;
}
.IM{ /* Icon More */
    font-size: 13px;
    background-color: #F5F5F5;
    color:#a6a6a6;
    margin:auto 0;
    padding:5px;
    border-radius: 4px;
}
</style>