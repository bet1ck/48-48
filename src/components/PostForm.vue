<template>
    <form @submit.prevent>
        <h4>Создание поста</h4>
        <MyInput
            v-model="post.title"
            type="text"
            class="input"
            placeholder="Название"
        />
        <MyInput
            v-model="post.body"
            type="text"
            class="input"
            placeholder="Описание"
        />
        <MyButtonVue
            style="align-self: flex-end; margin-top: 15px"
            @click="createPost"
        >
            Создать    
        </MyButtonVue>
    </form>
</template>

<script>
export default {
    data(){
        return{
            post: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now(); 
            this.$emit ('create' , this.post)
            this.post = {
                title: '',
                body: '',
            }
        }
    }
}
</script>

<style>
form
{
	display: flex;
	flex-direction: column;
}

</style>