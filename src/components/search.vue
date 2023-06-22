<template>
    <div class="BS">
        <div class="S">
            <input class="SI" type="text" placeholder="دنبال چه چیزی میگردی؟">
            <div class="C">
                <span>در دسته بندی</span>
                <span class="fontIcon">&#xe910;</span>
            </div>
            <div class="fontIcon IS">&#xe901;</div>
        </div>
    </div>
</template>
<style scoped>
.BS{ /* Container Search */
    padding: 50px;
    border-radius: 10px;
    background-color: #FFF;
}
.S{ /* Search */
    background-color: #F5F5F5;
    display: grid;
    grid-template-columns: 2fr 160px 100px;
    gap:10px;
    border-radius: 10px;
    align-items: center;
}
.IS{ /* Icon Search */
    font-size: 30px;
    opacity: .5;
    text-align: center;
    background-color: #ededed;
    padding: 20px 0;
    border-radius: inherit;
    cursor: pointer;
}
.C{ /* Category */
    color:var(--CPrimary);
    display: flex;
    align-items: center;
    justify-content: space-around;
    border-right: 1px solid var(--CPrimary);
    cursor: pointer;
}
.SI{ /* Search Input */
    background-color: #F5F5F5;
    outline: none;
    border: none;
    margin:0 50px;
    font-family: vazir;
    font-weight: bold;
    font-size: 18px;
}
.SI::placeholder{
    color:#000;
}
</style>