<template>
    <div class="app">
        <form @submit.prevent>
            <input 
                v-model="post.title"
                class='input' 
                type="text" 
                placeholder="Название"
            >
            <input 
                v-model="post.body"
                class='input' 
                type="text" 
                placeholder="Описание"
            >
            <button class="button" @click="createPost" >Создать</button>
        </form>
    </div>
</template>

<script setup>
export default {
    data() {
        return {
            post: {
                title: '', 
                body: '',
            }
        }
    }, 
    methods: {
        createPost() {
            this.post.id=Date.now();
            this.$emit('create', this.post)
            this.post = {
                title: '', 
                body: '',
            }
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
form {
    display: flex;
    flex-direction: column;
}
.app {
    padding: 20px;
}
.button {
    margin-top: 15px;
    color: white;
    width: 170px;
    height: 40px;
    border-radius: 10px;
    background-color: teal;
    font-size: large;
    font-weight: bold;
    font-style: italic;
    text-align: center;
    align-self: flex-end;
}
.input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
}
</style>