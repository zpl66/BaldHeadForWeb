<template>
    <nav class="navbar navbar-expand-lg navbar-blur">
        <div class="container">
            <router-link class="navbar-brand" :to="{ name: 'home' }">Whisper Space</router-link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText"
                aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarText">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <!-- 左侧导航项 -->
                    <li class="nav-item">
                        <router-link class="nav-link active" aria-current="page"
                            :to="{ name: 'home' }">Home</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" :to="{ name: 'friends' }">Friends</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" :to="{ name: 'feed' }">Feed</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" :to="{ name: 'about' }">About</router-link>
                    </li>
                </ul>
                <ul class="navbar-nav">
                    <!-- 右侧导航项 -->
                    <li class="nav-item">
                        <router-link class="nav-link" :to="{ name: 'login' }">Login</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" :to="{ name: 'register' }">Register</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: "NavBar",

}
</script>

<style scoped>
.navbar-blur {
    background-color: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
}

.navbar {
    border-radius: 10px;
    cursor: url('/public/cursors/work.png') 16 16, auto;
}
</style>
