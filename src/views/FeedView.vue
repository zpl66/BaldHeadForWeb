<template>
    <ContentBase>
        <div class="row">
            <div class="col-4">
                <FeedInfo @follow="follow" @unfollow="unfollow" :user="user" :posts="posts" />
                <FeedWrite @post_a_post="post_a_post" />
            </div>
            <div class="col-8">
                <FeedPosts :posts="posts" />
            </div>
        </div>
    </ContentBase>
</template>
<script>
import ContentBase from '@/components/ContentBase.vue';
import FeedInfo from '@/components/feed/FeedInfo.vue';
import FeedPosts from '@/components/feed/FeedPosts.vue';
import FeedWrite from '@/components/feed/FeedWrite.vue';
import { reactive } from 'vue';
export default {
    name:'FeedView',
    components: {
        ContentBase,
        FeedInfo,
        FeedPosts,
        FeedWrite,
    },
    setup() {
        const user = reactive({
            id: 1,
            userName: "喵喵喵",
            lastName: "喵",
            firstName: "喵喵",
            followerCount: 200,
            is_followed: false,
        });
        const posts = reactive({
            Count: 0,
            posts: [
              
            ]
        });
        const follow = () => {
            if (user.is_followed) return;
            user.is_followed = true;
            user.followerCount++;
        };
        const unfollow = () => {
            if (!user.is_followed) return;
            user.is_followed = false;
            user.followerCount--;
        };
        const post_a_post = (content) => {
            posts.Count++;
            posts.posts.unshift({
                id: posts.Count,
                userId: 1,
                content: content,
            })
        };
        return {
            user,
            follow,
            unfollow,
            posts,
            post_a_post
        }
    }
}
</script>
<style scoped></style>
