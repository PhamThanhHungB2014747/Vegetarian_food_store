<template>
    <div class="login-form">
        <form @submit.prevent="login()">
            <h1 class="text-center">Sign In</h1>
            <div class="content">
                <ul class="ul_form">
                    <li>
                        <div class="input-field">
                            <input type="email" v-model="user.email" placeholder=" Email" autocomplete="nope"
                                @blur="validate()" :class="{ 'is-invalid': errors.email }">
                            <div class="invalid-feedback" v-if="errors.password">
                                {{ errors.email }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="password" v-model="user.password" placeholder=" Password"
                                autocomplete="new-password" @blur="validate()" :class="{ 'is-invalid': errors.password }">
                            <div class="invalid-feedback" v-if="errors.password">
                                {{ errors.password }}
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="d-flex justify-content-around">
                <button type="submit" class="btn btn-primary" style="width:40%">Đăng Nhập</button>
                <button @click="goToRegister($event)" class="btn btn-primary" style="width:40%">Đăng Ký</button>
            </div>
        </form>
        <br>
        <div class="d-flex justify-content-center">
            <button @click="goToIndex($event)" class="btn btn-success" style="width:90%">Quay Lại</button>
        </div>
    </div>
</template>
  
<script>
import UserService from "../services/user.service";

export default {
    data() {
        return {
            errors: {
                email: "",
                password: "",
            },
            user: {
                email: "",
                password: "",
            },
        }
    },
    methods: {
        validate() {
            let isValid = true;

            this.errors = {
                email: "",
                password: "",
            };
            if (!this.user.email) {
                this.errors.email = "Email là bắt buộc";
                isValid = false;
            }
            if (!this.user.password) {
                this.errors.password = "Mật khẩu là bắt buộc";
                isValid = false;
            }
            return isValid;
        },
        goToRegister(event) {
            event.preventDefault();
            this.$router.push('/register');
        },
        goToIndex(event) {
            event.preventDefault();
            this.$router.push('/');
        },
        async login() {
            if (this.validate()) {
                const userLogin = await UserService.login(this.user);
                if (userLogin.role === "user") {
                    this.$store.commit('login');
                    this.$store.commit('setRole', 'user');
                    this.$store.commit('setName', userLogin.name);
                    this.$store.commit('setID', userLogin.id);
                    this.$router.push({ name: "index" });
                } else if (userLogin.role === "admin") {
                    this.$store.commit('login');
                    this.$store.commit('setRole', 'admin');
                    this.$store.commit('setName', 'admin');
                    this.$store.commit('setID', userLogin.id);
                    this.$router.push({ name: "index" });
                } else {
                    alert("Xin lỗi! Bạn đã nhập sai email hoặc mật khẩu!");
                }
            }
        }
    }
};
</script>
  

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    -webkit-font-smoothing: antialiased;
}

body {
    /* background: #e35869; */
    font-family: 'Rubik', sans-serif;
}

.invalid-feedback {
    text-align: left;
    color: red;
    margin-top: 5px;
}

.login-form {
    background: #fff;
    width: 500px;
    margin: 65px auto;
    display: -webkit-box;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    border-radius: 4px;
    box-shadow: 0 2px 25px rgba(0, 0, 0, 0.2);
}

.login-form h1 {
    padding: 35px 35px 0 35px;
    font-weight: 300;
}

.login-form .content {
    padding: 0 30px;
    text-align: center;
}

.login-form .input-field {
    padding: 12px 5px;
}

.login-form .input-field input {
    font-size: 16px;
    display: block;
    font-family: 'Rubik', sans-serif;
    width: 440px;
    padding: 8px 0;
    border: 1px solid royalblue;
    border-radius: 8px;
    outline: none;
}

.login-form .input-field input:focus {
    border-color: #222;
}

.ul_form {
    list-style-type: none;
    padding-left: 0;
}
</style>