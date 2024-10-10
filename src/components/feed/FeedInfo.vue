<template>
    <div class="card">
        <div class="card-body">
            <div class="row">
                <div class="col-5">
                    <img class="img-fluid" src="@/assets/OIP.jpg" alt="用户头像" >
                </div>
                <div class="col-7">
                    <div class="username">
                        {{ fullName }}
                    </div>
                    <div class="fans" style="font-size: 10px;" >
                        Followers: {{ user.followerCount }}
                    </div>
                    <div class="posts" style="font-size: 10px;">
                        Posts: {{ posts.Count || 0 }}
                    </div>
                    <button v-if="!user.is_followed" @click="follow" type="button"
                        class="btn btn-info btn-sm" >+follow</button>
                    <button v-if="user.is_followed" @click="unfollow" type="button"
                        class="btn btn-secondary btn-sm">-unfollow</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { computed } from 'vue';
export default {
    name: "FeedInfo",
    props: {
        user: {
            type: Object,
            required: true,
        },
        posts: {  
        type: Object,
        required: true,  
    },  
    },
    setup(props, context) {
        let fullName = computed(() => props.user.lastName + ' ' + props.user.firstName);
        const follow = () => {
            context.emit("follow");
        }
        const unfollow = () => {
            context.emit("unfollow");
        }
        return {
            fullName,
            follow,
            unfollow
        }
    }
}
</script>
<style scoped>
img {
    border-radius: 100%;
    width: 50px;
    height: 50px;
}
.username {
    font-weight: bold;
    font-size: smaller;
}
button {
    padding: 1px 2px;
    font-size: 12px;
}
.card {
    opacity: 0.7;
}
</style>