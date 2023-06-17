<script>
import headr from '../components/header.vue';
import slider from '../components/slider.vue';
export default{
    components:{headr,slider}
}
</script>
<template>
    <headr/>
    <div class="CM">
        <div class="container">
            <slider/>
        </div>
    </div>
</template>
<style scoped>
.CM{ /* Container Main */
    background-color: #f1f1f1;
    border: 5px solid #ffffff;
    border-radius: 8px;
    height: 100vh;
}
</style>