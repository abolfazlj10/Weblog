<script>
export default{
    props:['txt','type']
}
</script>
<template>
    <div v-if="type == 'side'" class="CTS">
        <div>
            <div class="T">{{ txt }}</div>
        </div>
        <div class="CB">
            <div class="FB FBS"></div>
            <div class="SB SBS"></div>
        </div>
    </div>
    <div v-else class="CT">
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

/* Side */
.CTS{ /* Container Title */
    font-size: 17px;
    font-family: vazirBold;
    color:#747474;
}
.CB{ /* Container Borders */
    display: flex;
    align-items: center; 
    gap:3px;
    margin-top: 5px;
}
.FBS{ /* First Border Sidebar*/
    width: 50px;
    height: 6px;
}
.SB{ /* Second Border Side */
    width: 17px;
    height: 6px;
}
</style>