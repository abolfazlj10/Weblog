<script>
export default{
    data(){
        return{
            post:[
                "photo_4_2023-06-14_12-33-11",
                "photo_2_2023-06-14_12-33-11",
                "photo_3_2023-06-14_12-33-11",
                "photo_1_2023-06-13_22-30-29",
                "photo_3_2023-06-13_22-25-10",
            ]
        }
    }
}
</script>
<template>
    <div class="CP">
        <div class="P" v-for="item in post">
            <div class="CIP"><div class="IP" :style="`background-image: url(../../public/${item}.jpg);`"></div></div>
            <div class="DP">
                <div class="TP">
                    <router-link to="/">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است.</router-link>
                    <div class="TPB"></div>
                </div>
                <div class="D">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است.چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد.کتابهای زیادی در شصت و سه درصد گذشته، حال و آینده شناخت فراوان جامعه و متخصصان را می طلبد تا با نرم افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی و فرهنگ پیشرو در ...</div>
                <div class="PI">
                    <div class="IT">
                        <div class="fontIcon">&#xe903;</div>
                        <div class="F">3 هفته پیش</div>
                    </div>
                    <div class="IT">
                        <div class="fontIcon">&#xe904;</div>
                        <div class="F">617 بازدید</div>
                    </div>
                    <div class="IT">
                        <div class="fontIcon">&#xe902;</div>
                        <div class="F">دسته فرانت اند</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.CP{ /* Container Post */
    display: flex;
    flex-direction: column;
    gap:10px;
}
.P{ /* Posts */
    background-color: #FFF;
    padding:15px;
    display: grid;
    grid-template-columns: 300px 3fr;
    gap:20px;
}
.P:hover .IP{
    transform:scale(1.1)
}
.CIP{ /* Container Image Post */
    width: inherit;
    height: 230px;
    overflow:hidden;
    border-radius: 8px;
}
.IP{ /* Image Post */
    width: 100%;
    height: 100%;
    background-size: cover;
    background-position: center;
    border-radius: inherit;
    transition:.1s ease all;
    cursor: pointer;
}
.DP{ /* Description Post */
    display: grid;
    grid-template-rows: 2fr 3fr 1fr;
}
.TP{ /* Title Post */
    font-size: 19px;
    padding-left: 100px;
    font-family: vazirBold;
    cursor: pointer;
    transition: .1s ease all;
}
.TP:nth-child(odd):hover{
    color:var(--CB);
}
.TPB{ /* Title Post Border */
    border-bottom: 1px dashed #00000018;
    height: 10px;
    width: 80%;
}
.D{ /* Description */
    font-size: 15px;
    padding-left:50px;
    color:#939494;
    align-self: center;
}
.PI{ /* Post Information */
    display: grid;
    grid-template-columns: repeat(3 , 100px);
    align-items: center;
}
.IT{ /* Icon Text */
    display: flex;
    gap:3px;
}
.F{ /* Font */
    font-size: 12px;
}
</style>