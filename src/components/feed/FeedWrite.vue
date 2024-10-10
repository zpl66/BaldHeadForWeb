<template>
    <div class="card edit-field">
        <div class="card-body">
            <div class="form-floating">
                <textarea v-model="content" class="form-control" placeholder="Leave a comment here" id="edit-field"
                    style="height: 100px"></textarea>
                <label for="edit-field">edit...</label>
                <button @click="post_a_post" type="button" class="btn btn-info btn-sm">post</button>
            </div>
        </div>
    </div>
</template>
<script>
import { ref } from 'vue';
export default {
    name: 'FeedWrite',
    setup(props, context) {
        let content = ref('');
        const post_a_post = () => {
            context.emit('post_a_post', content.value);
            content.value = "";
        };
        return {
            content,
            post_a_post
        }
    }
}
</script>
<style scoped>
.card {
    margin-top: 10px;
    opacity: 0.7;
}
.btn {
    float: right;
}
</style>



