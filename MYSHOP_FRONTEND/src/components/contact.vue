<template>
    <body>
        <div class="container">
            <div class="innerwrap">
                <section class="section1 clearfix">
                    <div class="textcenter">
                        <h1><span class="shtext">Liên hệ</span></h1>
                    </div>
                </section>
                <section class="section2 clearfix">
                    <div class="col2 column1 first">
                        <iframe
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3928.8415184420483!2d105.76804037592433!3d10.029933690077037!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31a0895a51d60719%3A0x9d76b0035f6d53d0!2zVHLGsOG7nW5nIMSQ4bqhaSBo4buNYyBD4bqnbiBUaMah!5e0!3m2!1svi!2s!4v1699971700132!5m2!1svi!2s"
                            width="100%" height="600" style="border:0;"  loading="lazy"
                            referrerpolicy="no-referrer-when-downgrade"
                            ></iframe>
                    </div>
                    <div class="col2 column2 last">
                        <div class="sec2innercont">
                            <div class="sec2addr">
                                <p>Đ.Trần Hưng Đạo, P.Bình Khánh, TP.Long Xuyên, An Giang</p>
                                <p><span class="collig">Phone :</span> +84 12345678</p>
                                <p><span class="collig">Email :</span> aulacchay@gmail.com</p>
                                <p><span class="collig">Fax :</span> +84 12345678</p>
                            </div>
                        </div>
                        <div class="sec2contactform">
                            <h3 class="sec2frmtitle">Muốn liên hệ với chúng tôi??</h3>
                            <form action="">
                                <div class="clearfix">
                                    <input class="col2 first" type="text" placeholder="Họ">
                                    <input class="col2 last" type="text" placeholder="Tên">
                                </div>
                                <div class="clearfix">
                                    <input class="col2 first" type="Email" placeholder="Email">
                                    <input class="col2 last" type="text" placeholder="Số điện thoại">
                                </div>
                                <div class="clearfix">
                                    <textarea name="textarea" id="" cols="30" rows="7">Nội dung</textarea>
                                </div>
                                <div class="clearfix"><input type="submit" value="Gửi"></div>
                            </form>
                        </div>

                    </div>
                </section>

            </div>
        </div>
    </body>
</template>
<style>
* {
    margin: 0px;
    padding: 0px;
}

*,
*:after,
*:before {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    -ms-box-sizing: border-box;
    -o-box-sizing: border-box;
    box-sizing: border-box;
}

.clearfix:before,
.clearfix:after {
    display: table;
    content: '';
}

.clearfix:after {
    clear: both;
}


body {
    background: #ffffff;
    color: #333;
    font-weight: normal;
    font-size: 1em;
    font-family: 'Roboto', Arial, sans-serif;
}

input:focus,
textarea:focus,
keygen:focus,
select:focus {
    outline: none;
}

::-moz-placeholder {
    color: #666;
    font-weight: 300;
    opacity: 1;
}

::-webkit-input-placeholder {
    color: #666;
    font-weight: 300;
}


/* Contact Form Styling */
.container {
    padding: 0 50px 70px;
}

.textcenter {
    text-align: center;
}

.section1 {
    text-align: center;
    display: table;
    width: 100%;
}

.section1 .shtext {
    display: block;
    margin-top: 20px;
}

.section1 .seperator {
    border-bottom: 1px solid #a2a2a2;
    width: 35px;
    display: inline-block;
    margin: 20px;
}

.section1 h1 {
    font-size: 40px;
    color: royalblue;
    font-weight: normal;
}

.section2 {
    width: 1200px;
    margin: 25px auto;
}

.section2 .col2 {
    width: 48.71%;
}

.section2 .col2.first {
    float: left;
}

.section2 .col2.last {
    float: right;
}

.section2 .col2.column2 {
    padding: 0 30px;
}

.section2 span.collig {
    color:grey;
    margin-right: 10px;
    display: inline-block;
    font-weight: 500;
}

.section2 .sec2addr {
    display: block;
    line-height: 26px;
}

.section2 .sec2addr p:first-child {
    margin-bottom: 10px;
}

.section2 .sec2contactform input[type="text"],
.section2 .sec2contactform input[type="email"],
.section2 .sec2contactform textarea {
    padding: 18px;
    border: 1px solid;
    background-color: #fff;
    margin: 7px 0;
}
.section2 .sec2contactform input[type="text"],
.section2 .sec2contactform input[type="email"],
.section2 .sec2contactform textarea:hover {
    border-color: royalblue;
}

.section2 .sec2contactform textarea {
    width: 100%;
    display: block;
    color: #666;
    resize: none;
    border: 1px solid;
}

.section2 .sec2contactform input[type="submit"] {
    padding: 15px 40px;
    color: #fff;
    border: 0;
    background: royalblue;
    font-size: 16px;
    text-transform: uppercase;
    margin: 7px 0;
    cursor: pointer;
    width: 100%;
}

.section2 .sec2contactform h3 {
    font-weight: normal;
    margin: 20px 0;
    margin-top: 30px;
    border-bottom: 1px solid #ddd;
    padding-bottom: 19px;
    color:royalblue;
}

/* @media querries */

@media only screen and (max-width: 1266px) {
    .section2 {
        width: 100%;
    }
}

@media only screen and (max-width: 960px) {
    .container {
        padding: 0 30px 70px;
    }

    .section2 .col2 {
        width: 100%;
        display: block;
    }

    .section2 .col2.first {
        margin-bottom: 10px;
    }

    .section2 .col2.column2 {
        padding: 0;
    }

    body .sec2map {
        height: 250px !important;
    }
}

@media only screen and (max-width: 768px) {
    .section2 .sec2addr {
        font-size: 14px;
    }

    .section2 .sec2contactform h3 {
        font-size: 16px;
    }

    .section2 .sec2contactform input[type="text"],
    .section2 .sec2contactform input[type="email"],
    .section2 .sec2contactform textarea {
        padding: 10px;
        margin: 3px 0;
    }

    .section2 .sec2contactform input[type="submit"] {
        padding: 10px 30px;
        font-size: 14px;
    }
}

@media only screen and (max-width: 420px) {
    .section1 h1 {
        font-size: 28px;
    }
}</style>