<template>
    <div class="register-container">
        <div class="register-box">
            <h2>REGISTER</h2>
            <div class="input-box">
                <label for="account">User Name:</label>
                <input type="text" id="account" v-model="account" placeholder="Enter your username...">
            </div>
            <div class="input-box">
                <label for="password">Password:</label>
                <input type="password" id="password" v-model="password" placeholder="Enter your password...">
            </div>
            <div class="input-box">
                <label for="confirmPassword">Confirm Your Password:</label>
                <input type="password" id="confirmPassword" v-model="confirmPassword"
                    placeholder="Enter your password again...">
            </div>
            <div class="input-box">
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="email" placeholder="Enter your email...">
            </div>
            <span v-if="errorMessage" class="error-message">{{ errorMessage }}</span>
            <button @click="register">Register</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "RegisterView",
    data() {
        return {
            account: '',
            password: '',
            confirmPassword: '',
            email: '',
            errorMessage: ''
        };
    },
    methods: {
        register() {
            if (this.password !== this.confirmPassword) {
                this.errorMessage = "Passwords do not match.";
            } else {
                this.errorMessage = "";
                alert("Registration successful!");
                // 此处可以加入表单提交或其他逻辑
            }
        }
    }
}
</script>

<style scoped>
/* 全屏居中容器 */
.register-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 3%;
}

/* 注册框样式 */
.register-box {
    width: 350px;
    padding: 40px;
    background-color: #00000060;
    border-radius: 10px;
    text-align: center;
}

/* 标题样式 */
h2 {
    color: #fff;
    margin-bottom: 30px;
}

/* 输入框容器 */
.input-box {
    margin-bottom: 20px;
    text-align: left;
}

/* 标签样式 */
.input-box label {
    display: block;
    color: #fff;
    margin-bottom: 5px;
}

/* 输入框样式 */
.input-box input {
    width: 100%;
    padding: 10px;
    border: none;
    background: transparent;
    border-bottom: 2px solid #fff;
    color: #fff;
    outline: none;
    font-size: 16px;
}

/* 按钮样式 */
button {
    width: 100%;
    padding: 12px;
    border: none;
    border-radius: 10px;
    color: #fff;
    font-size: 16px;
    background-image: linear-gradient(to right, #30cfd0, #330867);
    cursor: pointer;
    margin-top: 30px;
}

/* 错误信息样式 */
.error-message {
    color: red;
    margin-bottom: 15px;
    display: block;
}
</style>
