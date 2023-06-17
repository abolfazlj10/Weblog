<script>
export default {
    data(){
        return{
            topic:[
                {title:'آموزش',icon:'&#xe90f;',color:'f2776d',colorL:'e8685d'},
                {title:'پرسش و پاسخ',icon:'&#xe90a;',color:'7a86f6',colorL:'6c78eb'},
                {title:'ترفند',icon:'&#xe907;',color:'34a7a2',colorL:'289b96'},
                {title:'اخبار',icon:'&#xe905;',color:'c276fb',colorL:'b46ceb'},
                {title:'مقالات',icon:'&#xe90c;',color:'f9ac62',colorL:'f4a151'},
                {title:'کتاب ها',icon:'&#xe90e;',color:'7aa0f9',colorL:'6f96f0'},
                {title:'پروژ ها',icon:'&#xf07b;',color:'2cc897',colorL:'1fbc8b'}
            ]
        }
    }
}
</script>
<template>
    <div class="CT">
        <div class="TI" v-for="item in topic" :style="`background-color:#${item.color};`">
            <div class="fontIcon FT" v-html="item.icon"></div>
            <div class="TT" >{{ item.title }}</div>
            <div class="LG" :style="`background-image: linear-gradient(rgba(0, 0, 0, 0),#${item.colorL}); `"></div>
        </div>
    </div>
</template>
<style scoped>
.CT{ /* Container Topic */
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(7,1fr);
    gap:30px;
}
.TI{ /* Topic Item */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    height: 250px;
    border-radius:25px;
    color:#FFF;
    font-size: 19px;
    position: relative;
    transition: .1s ease all;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
}
.TI:hover{
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 20px 20px -1px;
    margin-top: -10px;
}
.FT{ /* Font Topic */
    font-size: 50px;
    z-index: 2;
    user-select: none;
}
.LG{ /* Leaier Gradient */
    height: 100%;
    width: 100%;
    position: absolute;   
    border-radius: 25px;
}
.TT{ /* Text Topic */
    z-index: 2;
}
</style>