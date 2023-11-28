<template>
    <nav class="navbar bg-success">
        <div class="navbar-container container d-flex justify-content-center align-items-center">
            <input type="checkbox" name="" id="">
            <div class="hamburger-lines">
                <span class="line line1"></span>
                <span class="line line2"></span>
                <span class="line line3"></span>
            </div>
            <ul class="menu-items">
                <router-link :to="{ name: 'boss' }"><li><a>Trang Chủ</a></li></router-link>
                <router-link :to="{ name: 'about' }"><li><a>Giới Thiệu</a></li></router-link>
                <router-link :to="{ name: 'products' }"><li v-if="!isUserRole"><a>Cửa Hàng</a></li></router-link>
                <li v-if="isLoggedIn && !isUserRole"><router-link :to="{name: 'cart'}"><a>Giỏ Hàng</a></router-link></li>
                <router-link :to="{ name: 'contact' }"><li><a>Liên Hệ</a></li></router-link>
                <li v-if="isUserRole" class="sign_in"><router-link to="/admin/products">Quản Trị</router-link></li>
                <li v-if="isLoggedIn">{{ this.$store.state.userName }}</li>
                <li v-if="isLoggedIn"><a @click="Log_out" href="#">Đăng Xuất</a></li>
                <div v-else>
                    <li class="sign_in"><router-link to="/login">Đăng Nhập</router-link></li>
                </div>
            </ul>
        </div>
    </nav>
</template>
<script>
export default {
    methods: {
        Log_out() {
            this.$store.commit('logout');
            this.$store.commit('setRole', '');
            this.$store.commit('setID', '');

        }
    },
    computed: {
        isLoggedIn() {
            return this.$store.state.isLoggedIn;
        },
        isUserRole() {
            return this.$store.state.role == 'admin';
        },
    },
    
};
</script>
<style>
.navbar input[type="checkbox"],
.navbar .hamburger-lines {
    display: none;
}

.container {
    max-width: 1200px;
    width: 90%;
    margin: auto;
}

.navbar {
    box-shadow: 0px 5px 10px 0px #aaa;
    position: fixed;
    width: 100%;
    color: #000;
    opacity: 0.85;
    z-index: 100;
}
.navbar-container {
    display: flex;
    justify-content:center;
    height: 54px;
    align-items: center;
}

.menu-items {
    display: flex;
    align-items: center; /* Căn giữa theo chiều dọc */
    margin: 0;
    padding: 0; 
    justify-content: center;
}
.menu-items li {
    list-style: none;
    margin: 0 1rem;
    font-size: 1.3rem;
    color: #fff;
}
.navbar a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease-in-out;
}

.navbar a:hover {
    cursor: pointer;
    background: royalblue;
    border-radius: 50px;
    padding: 8px;
}
.sign-in:hover {
    background: royalblue;
    border-radius: 50px;
}
@media (max-width: 768px) {
    .navbar {
        opacity: 0.95;
    }

    .navbar-container input[type="checkbox"],
    .navbar-container .hamburger-lines {
        display: block;
    }

    .navbar-container {
        display: block;
        position: relative;
        height: 64px;
        justify-content: space-between;
    }

    .navbar-container input[type="checkbox"] {
        position: absolute;
        display: block;
        height: 32px;
        width: 30px;
        top: 20px;
        left: 20px;
        z-index: 5;
        opacity: 0;
        cursor: pointer;
    }

    .navbar-container .hamburger-lines {
        display: block;
        height: 28px;
        width: 35px;
        position: absolute;
        top: 20px;
        left: 20px;
        z-index: 2;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .navbar-container .hamburger-lines .line {
        display: block;
        height: 4px;
        width: 100%;
        border-radius: 10px;
        background: #333;
    }

    .navbar-container .hamburger-lines .line1 {
        transform-origin: 0% 0%;
        transition: transform 0.3s ease-in-out;
    }

    .navbar-container .hamburger-lines .line2 {
        transition: transform 0.2s ease-in-out;
    }

    .navbar-container .hamburger-lines .line3 {
        transform-origin: 0% 100%;
        transition: transform 0.3s ease-in-out;
    }

    .navbar .menu-items {
        padding-top: 100px;
        background: #fff;
        height: 100vh;
        max-width: 300px;
        transform: translate(-150%);
        display: flex;
        flex-direction: column;
        margin-left: -40px;
        padding-left: 40px;
        transition: transform 0.5s ease-in-out;
        box-shadow: 5px 0px 10px 0px #aaa;
        overflow: scroll;
    }

    .navbar .menu-items li {
        margin-bottom: 1.8rem;
        font-size: 1.1rem;
        font-weight: 800;
    }

    .navbar-container input[type="checkbox"]:checked~.menu-items {
        transform: translateX(0);
    }

    .navbar-container input[type="checkbox"]:checked~.hamburger-lines .line1 {
        transform: rotate(45deg);
    }

    .navbar-container input[type="checkbox"]:checked~.hamburger-lines .line2 {
        transform: scaleY(0);
    }

    .navbar-container input[type="checkbox"]:checked~.hamburger-lines .line3 {
        transform: rotate(-45deg);
    }

}

@media (max-width: 500px) {
    .navbar-container input[type="checkbox"]:checked~.logo {
        display: none;
    }
}
</style>