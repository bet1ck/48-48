<template>
	<div class="app">
		<PostForm 
			@create = "createPost"
		/>
		<PostList
			:posts="posts"
		/>
	</div> 
</template>

<script>
import PostForm from "./components/PostForm";
import PostList from "@/components/PostList"

export default {
	components: {
		PostList, PostForm
	},
	data(){
		return{
			posts: [
				{id: 1,title: 'js1', body: 'описание поста'},
				{id: 2,title: 'js2', body: 'описание поста'},
				{id: 3,title: 'js3', body: 'описание поста'},
			],
		}
	},
	methods:{
		createPost(post)
			{
				console.log(post);
			},
		}
	}
</script>

<style>
*{
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

.app
{
	padding: 20px;
}

</style>