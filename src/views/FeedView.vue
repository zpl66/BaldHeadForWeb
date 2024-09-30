<template>
    <ContentBase>

        <div class="row">
            <div class="col-3">
                <div class="container">
                    <FeedInfo @follow="follow" @unfollow="unfollow" :user="user" />
                    <FeedPosts @post_a_post="post_a_post" />
                </div>
            </div>
            <div class="col-9">
                <div class="container">
                    <FeedWrite :posts="posts" />
                </div>
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
    name: "FeedView",
    components: {
        ContentBase,
        FeedInfo,
        FeedPosts,
        FeedWrite,
    },

    setup() {
        const user = reactive({
            id: 1,
            userName: "Percy Bysshe Shelley",
            lastName: "Shelley",
            firstName: "Percy Bysshe",
            followerCount: 0,
            is_followed: false,
        });

        const posts = reactive({
            count: 2,
            posts: [
                {
                    id: 1,
                    userId: 1,
                    content: "If the winter comes, can Spring be far behind?"
                },
                {
                    id: 2,
                    userId: 1,
                    content: "In the past belonged to the god of death, in the future will belong to you"
                }
            ]
        });

        function follow() {
            if (user.is_followed) return;
            user.is_followed = true;
            user.followerCount++;
        }

        function unfollow() {
            if (!user.is_followed) return;
            user.is_followed = false;
            user.followerCount--;
        }

        function post_a_post(content) {
            posts.count++;
            posts.posts.unshift({
                id: posts.count,
                userId: 1,
                content: content,
            })
        }

        return {
            follow,
            unfollow,
            post_a_post,
        }
    }
}
</script>

<style scoped></style>