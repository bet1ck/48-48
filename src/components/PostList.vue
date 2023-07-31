<template>
    <div v-if="posts.length>0  ">
        <h3>Список постов</h3>
        <PostItem
            :key="post.id"
            :post="post"
            v-for="post in posts"
            @remove="$emit('remove', post)"
        />
    </div>
    <h2 v-else style="color: red">
        Список постов пуст
    </h2>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
    components: { PostItem },
    props: {
        posts: {
            type: Array,
            required: true, 
        }
    }
}
</script>

<style>

</style>