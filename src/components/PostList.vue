<template>
    <div>
        <h3>Список пользователей</h3>
        <post-item :key="post.id" v-for="post in posts">
    </div>
</template>

<script>
export default {
    component: { PostItem },
    props: {
        posts: {
            type: Array,
            required: true, 
        }
    }
}
</script>

<style>
.post 
{
	padding: 15px;
	border: 2px solid teal;
	margin-top: 15px;
}
</style>