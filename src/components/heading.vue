<script>
export default{
    props:['txt']
}
</script>
<template>
    <div class="CT">
        <div class="FB"></div>
        <div class="SB"></div>
        <div class="T">{{ txt }}</div>
    </div>
</template>
<style scoped>
.CT{ /* Container Title */
    font-size: 20px;
    font-family: vazirBold;
    display: flex;
    align-items: center;
    gap:3px;
    margin:25px 0;
    color:#747474
}
.T{
    margin-right: 5px;
}
.FB{ /* First Border */
    background-color: #515151;
    height: 7px;
    width: 25px;
    border-radius: 10px;
}
.SB{ /* Second Border */
    background-color: #227ae5;
    height: 7px;
    width: 13px;
    border-radius: 10px;
}
</style>