<template>
    <div class="login-form">
        <form @submit.prevent="register()">
            <h1 class="text-center">Sign Up</h1>
            <div class="content">
                <ul class="ul_form">
                    <li>
                        <div class="input-field">
                            <input type="email" v-model="user.email" placeholder=" Email" autocomplete="nope"
                                @blur="validate()" :class="{ 'is-invalid': errors.email }">
                            <div class="invalid-feedback" v-if="errors.email">
                                {{ errors.email }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.name" placeholder=" Họ và tên" autocomplete="nope"
                                @blur="validate()" :class="{ 'is-invalid': errors.name }">
                            <div class="invalid-feedback" v-if="errors.name">
                                {{ errors.name }}
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
                    <li>
                        <div class="input-field">
                            <input type="password" v-model="user.confirmPassword" placeholder=" Confirm password"
                                @blur="validate()" :class="{ 'is-invalid': errors.confirmPassword }"
                                >
                            <div class="invalid-feedback" v-if="errors.confirmPassword">
                                {{ errors.confirmPassword }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.address" placeholder=" Địa chỉ"
                                @blur="validate()" :class="{ 'is-invalid': errors.address }"
                            >
                            <div class="invalid-feedback" v-if="errors.address">
                                {{ errors.address }}
                            </div>
                        </div>
                    </li>
                    <li>
                        <div class="input-field">
                            <input type="text" v-model="user.phoneNumber" placeholder=" Số điện thoại"
                                @blur="validate()" :class="{ 'is-invalid': errors.phoneNumber }"
                            >
                            <div class="invalid-feedback" v-if="errors.phoneNumber">
                                {{ errors.phoneNumber }}
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="d-flex justify-content-around">
                <button @click="goToLogin($event)" class="btn btn-success" style="width:40%">Quay Lại</button>
                <button type="submit" class="btn btn-primary" style="width:40%">Đăng Ký</button>
            </div>
        </form>
    </div>
</template>
  
<script>
import UserService from "../services/user.service";
export default {
    data() {
        return {
            errors: {
                email: "",
                name: "",
                password: "",
                confirmPassword: "",
                address: "",
                phoneNumber: "",
            },
            user: {
                email: "",
                name: "",
                password: "",
                confirmPassword: "",
                address: "",
                phoneNumber: "",
            },
        }
    },
    methods: {
        validate() {
            let isValid = true;

            this.errors = {
                email: "",
                password: "",
                confirmPassword: "",
            };
            if (!this.user.email) {
                this.errors.email = "Email là bắt buộc";
                isValid = false;
            }
            if (!this.user.name) {
                this.errors.name = "Họ và tên là bắt buộc";
                isValid = false;
            }
            if (!this.user.password) {
                this.errors.password = "Mật khẩu là bắt buộc";
                isValid = false;
            }
            if (this.user.confirmPassword != this.user.password) {
                this.errors.confirmPassword = "Mật khẩu chưa đúng";
                isValid = false;
            }
            if(!this.user.address){
                this.errors.address = "Địa chỉ là bắt buộc";
                isValid = false;
            }
            if( !this.user.phoneNumber){
                this.errors.phoneNumber = "Số điện thoại là bắt buộc";
                isValid = false;
            }
            return isValid;
        },
        goToLogin(event) {
            event.preventDefault();
            this.$router.push('/login');
        },
        async register() {
            if (this.validate()) {
                try {
                    await UserService.create(this.user);
                    alert(
                        `Chúc mừng ${this.user.name} !!! Bạn đã đăng ký tài khoản thành công!`
                    );
                    this.$router.push({ name: "login" });
                } catch (error) {
                    console.log(error);
                }
            }
        },
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
    width: 430px;
    padding: 8px 0;
    border: 1px solid royalblue;
    outline: none;
}
.login-form .input-field input:focus {
    border-color: #222;
}
.ul_form {
    list-style-type: none;
    /* Loại bỏ dấu chấm đầu */
    padding-left: 0;
    /* Loại bỏ khoảng cách trái của danh sách */
}
</style>