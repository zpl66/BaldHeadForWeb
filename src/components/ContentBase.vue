<template>
    <div class="container">
        <div class="card">
            <div class="card-body">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ContentBase",

}
</script>

<style scoped>
.container {
    margin-top: 20px;
    cursor: url('/public/cursors/work.png') 16 16, auto;
}

.card {
    background-color: rgba(255, 255, 255, 0.6);
    /* 半透明背景 */
    backdrop-filter: blur(5px);
    /* 轻微毛玻璃效果 */
    border-radius: 10px;
    padding: 20px;
}
</style>
