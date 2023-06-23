<script>
import boxDropDown from './boxDropDown.vue';
export default{
    components:{boxDropDown}
}
</script>
<template>
    <div class="SB">
        <boxDropDown head="دسته بندی">
            <div class="test">    
                <div v-for="i in 5">{{ i }}</div>
            </div>
        </boxDropDown>
    </div>
</template>
<style scoped>
.SB{ /* SideBar */
    display: flex;
    flex-direction: column;
    gap:10px;
}
.test{
    margin:20px 0;
}
</style>