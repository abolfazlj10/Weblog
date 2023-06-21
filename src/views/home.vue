<script>
import headr from '../components/header.vue';
import slider from '../components/slider.vue';
import topics from '../components/topics.vue';
import message from '../components/message.vue';
import search from '../components/search.vue'
export default{
    components:{headr,slider,topics,message,search}
}
</script>
<template>
    <headr/>
    <div class="CM">
        <div class="container">
            <slider/>
        </div>
        <div class="container">
            <topics/>
        </div>
        <div class="container">
            <message/>
        </div>
        <div class="container CC">
            <search/>
            <div>category</div>
        </div>
    </div>
</template>
<style scoped>
.CM{ /* Container Main */
    background-color: #f4f4f4;
    border: 5px solid #ffffff;
    border-radius: 8px;
    height: 1900px;
}
.CC{ /* Container Content */
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap:60px;
    margin-top: 30px;
}
.CC > *{
    background: #FFF;
}
</style>