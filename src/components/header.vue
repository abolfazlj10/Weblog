<script>
export default{
    data(){
        return{
            itemHead:[
                "صفحه اصلی",
                "پرسش و پاسخ",
                "آموزش",
                "ترفند",
                "اخبار",
                "درباره ما"
            ]
        }
    }
}
</script>
<template>
    <div class="container CH">
        <div class="TW"><router-link to="/">WebBlog</router-link></div>
        <div class="NB">
            <div v-for="item in itemHead"><routerLink to="/">{{ item }}</routerLink></div>
        </div>
        <div class="SL">
            <router-link to="/" class="BL">
                <div class="fontIcon IL">&#xe900;</div>
                <div>ورود</div>
                <div class="BLS"></div>
                <div>عضوریت</div>
            </router-link>
        </div>
    </div>
</template>
<style scoped>
.CH{ /* Conitaner Header */
    display: grid;
    grid-template-columns: 1fr 6fr 1fr;
    margin-top: 10px;
    padding:10px 0;
    align-items:center;
}
.NB{ /* NavBar */
    display: flex;
    gap:50px;
    font-size: 14px;
}
.SL{ /* Sign in and Login */
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 15px;
}
.TW{ /* Title Weblog */
    font-size: 35px;
    background-image: linear-gradient(to right,var(--CB) 70%,black);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-family: vazirbold;
}
.BL{ /* Button Login */
    background-color: var(--CB);
    color:#fff;
    display: flex;
    border-radius: 9px;
    padding:8px 15px;
    gap:5px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 6px -1px, rgba(0, 0, 0, 0.06) 0px 2px 4px -1px;
}
.IL{ /* Icon Login*/
    margin: auto;
    font-size: 23px;
}
.BLS{ /* Border Login Signin*/
    width: 1px;
    background-color: #ffffffa7;
}
</style>