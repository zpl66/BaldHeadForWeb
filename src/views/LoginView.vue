<template>
    <div class="login-container">
        <div class="login-box">
            <h2>LOGIN</h2>
            <div class="input-box">
                <label for="account">Account:</label>
                <input type="text" id="account" placeholder="Enter your username or email...">
            </div>
            <div class="input-box">
                <label for="password">Password:</label>
                <input type="password" id="password" placeholder="Enter your password...">
            </div>
            <button>Log in</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "LoginView",
    components: {}
}
</script>

<style scoped>
/* 全屏居中容器 */
.login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 5%;
}

/* 登录框样式 */
.login-box {
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
</style>