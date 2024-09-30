<template>
    <div class="container">
        <div class="card">
            <div class="card-body">
                <div class="form-floating">
                    <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea2"
                        style="height: 100px"></textarea>
                    <label for="floatingTextarea2">edit...</label>
                    <button type="button" class="btn btn-primary btn-sm">post</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FeedPosts',
}
</script>

<style scoped>
.container {
    margin-top: 10px;
}

button {
    margin: 10px;
    float: right;
}
</style>