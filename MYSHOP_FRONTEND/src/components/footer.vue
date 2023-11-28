<template>
    <footer class="row bg-success text-white">
        <div class="col-sm-4 p-5 ml-5 pl-5 content text-decoration-none">
            <h3 class="list-group mb-1">Vegetarian food store</h3>
            <li class="list-group-item mb-1"><router-link to="">Trang Chủ</router-link></li>
            <li class="list-group-item mb-1"><router-link to="">Cửa Hàng</router-link></li>
            <li class="list-group-item mb-1"><router-link to="">Giới Thiệu</router-link></li>
            <li class="list-group-item"><router-link to="">Liên Hệ</router-link></li>
        </div>
        <div class="col-sm-4 p-5 ml-5">
            <h3 class="list-group mb-1">Điều khoản dịch vụ</h3>
            <li class="list-group-item mb-1">Chính sách bảo mật</li>
            <li class="list-group-item mb-1">Mua hàng</li>
            <li class="list-group-item mb-1">Đổi trả</li>
        </div>
        <div class="col-sm-4 p-5 ml-5 content">
            <h3 class="list-group mb-1">Chi tiết liên hệ</h3>
            <li class="list-group-item mb-1"><a href="#"><i class="fa-brands fa-facebook"></i> Facebook</a></li>
            <li class="list-group-item mb-1"><a href="#"><i class="fa-brands fa-google"></i> Google</a></li>
            <li class="list-group-item"><a href="#"><i class="fa-brands fa-twitter"></i> Twitter</a></li>
        </div>
        <div class="bg-secondary col-sm-12 d-flex align-items-center justify-content-center">
            <p>&copy; B2014747_CT271&commat;gmail.com</p>
        </div>
    </footer>
   <!-- eslint-disable -->
</template>

<style media="screen">
footer {
    position: absolute;
    height: auto;
    width: 100vw;
}
.content a :hover{
    color: royalblue;
}
.content li:hover {
    color: royalblue;
}
@media (max-width:500px) {
    .footer-menu ul {
        display: flex;
        margin-top: 10px;
        margin-bottom: 20px;
    }
}
</style>
