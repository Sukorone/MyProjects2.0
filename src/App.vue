<template>
    <div class="app">
        я хуесос
        <post-form @create="createPost"/>
        <post-list :posts="posts"/>
    </div>
</template>
 
<script>
import postForm from './components/postForm.vue';
import postFormVue from './components/postForm.vue';
import PostList from './components/postList.vue';
import postListVue from './components/postList.vue';
export default {
    components: { 
        postForm, PostList 
    },
    data() {
        return {
            posts: [
                {id: 1 , title: 'Javascript', body: 'Описание поста'},
                {id: 2 , title: 'Javascript 2', body: 'Описание поста 2'}, 
                {id: 3 , title: 'Javascript 3', body: 'Описание поста 3'},
            ], 
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        }
    }
}
</script>

<style>

</style>