<script>
export default{
    data(){
        return{
            user:'نوشته شده توسط ابوالفضل',
            brand:'DEVELOPoGIST',
            dateAdd:'چهارشنبه ، 22 خرداد 1401',
            desc:[
                "",
                "انتشار React 18 - ویژگی‌های نسخه‌ی جدید ری‌اکت",
                "قالب‌های گیت هاب برای درخواست‌های Pull یکپارچه و هوشمندانه",
                "انگولار یا ویو  | مقایسه دو فریمورک جاواسکریپت"
            ],
            loremI:'لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. ',
        }
    }
}
</script>
<template>
    <div class="CH">
        <div class="NB">
            <router-link to="/"><div class="B">{{ brand }}</div></router-link>
            <div class="RN">
                <div><div class="RNB"></div><router-link to="/">مطالب </router-link></div>
                <div><div class="RNB"></div><router-link to="/">انتشار مطلب </router-link></div>
                <div><div class="RNB"></div><router-link to="/">درباره ما </router-link></div>
                <div><div class="RNB"></div><router-link to="/">ارتباط با ما </router-link></div>
            </div>
            <div class="CL">
                <router-link to="/"><div class="LB">ورود</div></router-link>
                <router-link to="/"><div class="SB">ثبت نام</div></router-link>
            </div>
        </div>
        <div class="CHB">
            <div class="TS">
                <div class="FTS">
                    <div class="TSB" v-for="i in 3" :class="i != 1 ? 'BTSB' : ''">
                        <div class="TSBC">
                            <div class="TTS"><router-link to="/">{{ desc[i] }}</router-link></div>
                            <div class="DB">{{ loremI }}</div>
                            <div class="DC">{{ dateAdd }}</div>
                        </div>
                        <div class="HS"><router-link to="/" class="ITS" :class="'ITS' + i"><div class="LI">{{ user }}</div></router-link></div>
                    </div>
                </div>
                <div class="COS">
                    <div class="HS"><router-link to="/" class="ITS ITS4"><div class="LI">{{ user }}</div></router-link></div>
                    <div class="TSBC">
                        <div class="TTS"><router-link to="/">{{ desc[3] }}</router-link></div>
                        <div class="DB">{{ loremI }}</div>
                        <div class="DC">{{ dateAdd }}</div>
                    </div>
                </div>
            </div>
            <div class="V"><img class="VT" src="../assets/img/vecteezy_cute-astronaut-working-as-a-programmer_ (2).png"></div>
            <!-- <div class="V"><img class="VT" src="../assets/img/vecteezy_programmer-people-concept-use-laptop-and-programming-code_.png"></div> -->
            <!-- <div class="V"><img class="VT" src="../assets/img/13426526.png"></div> -->
        </div>
    </div>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bungee+Shade&display=swap');
.CH{ /* Container Header */
    height: 700px;
    color:var(--CPrimary);
    background-color: #DDE6ED;
    margin:10px;
    border-radius: 5px;
    padding:10px 5px;
    font-weight: bold;
    display: flex;
    flex-direction:column;
}
.NB{ /* NavBar */
    display: grid;
    align-items: center;
    grid-template-columns: 1fr 4fr 4fr;
    padding:0 10px;
    margin:5px 10px;
    border-bottom: 1px solid var(--border);
    font-size: 18px;
}
.RN{ /* Right NavBar */
    display: flex;
    justify-content: space-evenly;
}
.RN > *{
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    position: relative;
}
.RN > *:hover .RNB{
    background-color: var(--CB);
    width: 100%;
}
.RNB{ /*Right NavBar Border */
    height: 1px;
    transition: .2s all ease;
    width: 0%;
    position: absolute;
    right:0;
    border-radius: 50%;
}
.B{ /* Brand */
    font-size: 20px;
    color:var(--CB);
    font-family: 'Bungee Shade', cursive;
    text-align: right;
}
.CL{ /* Container Login */
    display: flex;
    justify-content: flex-end;
    gap:10px;
}
.LB{ /* Login Button */
    background-color: #fff;
    border-radius: 5px;
    padding: 3px 15px;
    color:var(--CB);
    border:1px solid #fff;
    transition: .1s all ease;
}
.LB:hover{
    background-color: var(--CB);
    color:#FFF;
    border: 1px solid var(--CB);
}
.SB{ /* Sign in Button */
    border: 1px solid var(--CB);
    color:var(--CB);
    padding: 3px 6px;
    border-radius: 5px;
    transition:.1s all ease;
}
.SB:hover{
    background-color: var(--CB);
    color:#fff;
}
.CHB{ /* Content Header Bottom */
    flex-grow: 1;
    display: grid;
    grid-template-columns: 2fr 1fr;
}
.VT{ /* Vectore Tag */
    width: 500px;
}
.V{ /* Vecotore */
    text-align: center;
    margin:auto;
}
.TS{ /* Three Slide */
    padding:10px;
    display: grid;
    grid-template-columns: 60% 1fr;
    gap: 5px;
}
.ITS{ /* Img Three Slide */
    background-position: center;
    background-size: cover;
    border-radius: 5px;
    display: block;
    width: 100%;
    height: 100%;
    transition:.1s all ease;
}
.TSB:hover .LI{
    opacity:1;
    padding:10px;
}
.TSB:hover .ITS{
    scale: 1.04;
}
.ITS1{
    background-image: url(../assets/img/photo_4_2023-06-14_12-33-11.jpg);
}
.ITS2{
    background-image: url(../assets/img/photo_3_2023-06-14_12-33-11.jpg);
}
.ITS3{
    background-image: url(../assets/img/photo_2023-06-14_12-49-30.jpg);
}
.ITS4{
    background-image: url(../assets/img/photo_1_2023-06-14_12-33-11.jpg);
}
.TSB{ /* Therr Slide Box */
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap:10px;
    padding:10px 5px;
    flex-grow: 1;
}
.HS{
    border-radius: 5px;
    overflow: hidden;
}
.BTSB{ /* Border Three Slide Box*/
    border-top:1px solid var(--border);
}
.TSBC{
    text-align: justify;
    display: flex;
    flex-direction: column;
    gap:20px;
}
.LI{ /* Lier Image */
    width: 100%;
    height: 100%;
    border-radius: 5px;
    background-image:linear-gradient(rgba(0, 0, 0, 0),rgb(0 0 0 / 18%));
    display: flex;
    align-items: end;
    justify-content: center;
    color:#DDE6ED;
    font-size: 10px;
    padding:5px;
    opacity: 0.5;
    transition:.1s all ease;
}
.DC{ /* Date Created */
    font-size: 12px;
    color:#27374da1;
    text-align: left;
}
.TTS{ /* Text Three Side */
    font-size: 20px;
    font-family: vazirbold;
    transition:.1s all ease;
}
.TTS:hover{
    color:var(--CB);
}
.DB{ /* Description Box */
    font-size: 14px;
}
.COS{ /* Container One Slide */
    display: grid;
    grid-template-rows: 2fr 1fr;
    gap:10px;
    padding:10px 5px;
}
.COS .DC{
    text-align: right;
}
.COS:hover .LI{
    opacity:1;
    padding:10px;
}
.COS:hover .ITS{
    scale: 1.04;
}
.FTS{ /* Flex Three Slide */
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}
</style>