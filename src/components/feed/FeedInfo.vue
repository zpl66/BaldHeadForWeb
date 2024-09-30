<template>
    <div class="container">
        <div class="card">
            <div class="card-body">
                <div class="row">
                    <div class="col-3" id="col-image">
                        <img src="@/assets/OIP.jpg" alt="用户头像">
                    </div>
                    <div class="col-9">
                        <div class="username">小黑子</div>
                        <div class="fans">关注：0</div>
                        <button type="button" class="btn btn-primary btn-sm">+关注</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FeedInfo",
}
</script>

<style scoped>
img {
    border-radius: 50%;
    width: 100%;
}

.container {
    margin-top: 10px;
}

button {
    margin: 10px;
}

.col-9 {
    text-align: center;
}

#col-image {
    padding: 0%;
}
</style>