<template>
    <div class="responsive-container-block bigContainer">
        <div class="responsive-container-block Container bottomContainer">
            <div class="ultimateImg">
                <img class="mainImg" src="https://aulac-vegan.com/wp-content/uploads/2020/08/gioi-thieu-2.jpg">
            </div>
            <div class="allText bottomText">
                <p class="text-blk subHeadingText">
                    TỔNG QUAN
                </p>
                <p class="text-blk" style="text-align:justify;">
                    Hơn 25 năm hình thành và phát triển , thương hiệu thực phẩm chay “Âu Lạc” đã 
                    khẳng định được uy tính của mình trên thị trường trong nước và quốc tế. Thương 
                    hiệu thực phẩm chay Âu Lạc đã tạo được uy tín hàng đầu Việt Nam về dây chuyền 
                    sản xuất thực phẩm chay. Với phương châm “chất lượng hàng đầu”, công ty cam kết 
                    luôn cung cấp những sản phẩm chất lượng cao nhất. Bên cạnh đó, vệ sinh an toàn 
                    thực phẩm cũng là tiêu chí hàng đầu mà Âu Lạc đặt ra trước khi đưa sản phẩm ra thị 
                    trường. Công ty luôn quan tâm đến sức khỏe của người tiêu dùng và công nghệ thân 
                    thiện với môi trường xanh.
                </p>
                <p class="text-blk" style="text-align:justify;">
                    Thực phẩm chay Âu Lạc hiện không chỉ có mặt trên khắp các chợ, siêu thị, nhà hàng 
                    Việt Nam, mà còn xuất khẩu sang các nước Mỹ, Canada, Úc, Đức , Anh… Sản phẩm 
                    công ty đa dạng phong phú và không ngừng cải tiến, nâng cao chất lượng. Công ty 
                    thực phẩm chay Âu Lạc đã đạt được nhiều thành tích và danh hiệu uy tín trong nước. 
                    Công ty luôn nỗ lực phấn đấu để xứng đáng với sự tin cậy của khách hàng, các đối 
                    tác trong và ngoài nước.
                </p>
            </div>
        </div>
    </div>
</template>
<style>
* {
    font-family: Nunito, sans-serif;
}

.responsive-container-block {
    min-height: 75px;
    height: fit-content;
    width: 100%;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    margin: 0 auto;
    justify-content: flex-start;
}

a {
    text-decoration-line: none;
    text-decoration-thickness: initial;
    text-decoration-style: initial;
    text-decoration-color: initial;
}

.text-blk {
    margin: 0;
    padding: 10px;
    line-height: 25px;
}

.responsive-container-block.bigContainer {
    /* padding: 10px 30px; */
    flex-direction: column;
    align-items: center;
    justify-content: center;
    /* padding: 10px 50px ; */
}

.mainImg {
    color: black;
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.allText {
    padding: 0;
    width: 40%;
    margin: 0;
}

.text-blk.subHeadingText {
    color: rgb(102, 102, 102);
    font-size: 26px;
    line-height: 32px;
    font-weight: 700;
}
.responsive-container-block.Container {
    margin: 50px auto;
    justify-content: center;
    align-items: center;
    max-width: 1320px;
    padding: 10px;
}

.responsive-container-block.Container.bottomContainer {
    flex-direction: row-reverse;
    margin: 50px auto;
    position: static;
}
.allText.bottomText {
    margin-right: 40px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding-right: 15px;
}
.ultimateImg {
    width: 50%;
    position: relative;
}

@media (max-width: 1024px) {
    .responsive-container-block.Container {
        max-width: 850px;
    }

    .mainImg {
        width: 55%;
        height: auto;
    }

    .allText {
        width: 40%;
        margin-left: 20px;
    }

    .responsive-container-block.bigContainer {
        padding: 10px;
    }

    .responsive-container-block.Container.bottomContainer {
        margin: 50px auto;
    }

    .responsive-container-block.Container {
        max-width: 830px;
    }

    .allText.bottomText {
        margin-top: 30px;
        margin-right: 40px;
        text-align: left;
    }

    .text-blk.subHeadingText {
        text-align: left;
        font-size: 26px;
        line-height: 32px;
    }

    .responsive-container-block.bigContainer {
        padding-top: 10px;
        padding-right: 30px;
        padding-bottom: 10px;
        padding-left: 30px;
    }

    .responsive-container-block.Container {
        justify-content: space-evenly;
    }

    .responsive-container-block.Container.bottomContainer {
        padding: 10px 0;
        max-width: 930px;
    }

    .allText.bottomText {
        width: 40%;
    }

    .mainImg {
        width: 100%;
    }
}

@media (max-width: 768px) {
    .allText {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0;
    }

    .responsive-container-block.Container {
        flex-direction: column;
        height: auto;
    }

    .text-blk.subHeadingText {
        text-align: center;
        font-size: 24px;
    }

    .allText {
        margin-top: 40px;
    }

    .responsive-container-block.Container {
        margin: 50px auto;
    }

    .responsive-container-block.Container.bottomContainer {
        margin: 50px auto;
    }

    .allText.bottomText {
        margin-top: 40px;
    }

    .mainImg {
        width: 100%;
        margin-bottom: -70px;
    }

    .responsive-container-block.Container.bottomContainer {
        flex-direction: column;
    }

    .ultimateImg {
        width: 100%;
    }

    .purpleBox {
        position: static;
    }

    .allText.bottomText {
        width: 100%;
        align-items: flex-start;
    }
    .text-blk.subHeadingText {
        text-align: left;
    }

    .ultimateImg {
        position: static;
    }

    .mainImg {
        margin: 0;
    }

    .ultimateImg {
        position: relative;
    }

    .allText.bottomText {
        margin-top: 100px;
        margin-right: 0px;
        margin-bottom: 0px;
        margin-left: 0px;
    }
}

@media (max-width: 500px) {
    .responsive-container-block.Container {
        padding: 10px 0;
        width: 100%;
        max-width: 100%;
    }

    .mainImg {
        width: 100%;
    }

    .responsive-container-block.bigContainer {
        padding: 10px 25px;
    }

    .text-blk.subHeadingText {
        font-size: 24px;
        padding: 0;
        line-height: 28px;
    }

    .allText {
        padding: 0;
        width: 100%;
    }

    .allText.bottomText {
        margin-top: 50px;
        padding: 0 ;
        margin-top: 30px;
    }

    .ultimateImg {
        position: static;
    }

    .allText.bottomText {
        margin-top: 75px;
    }

    .responsive-container-block.bigContainer {
        padding: 10px 20px;
    }
}
</style>