<template>
    <div class="post" v-for="post in posts">
        <div class=""><strong>Навание:</strong>{{post.title}}</div>
        <div class=""><strong>Описание:</strong>{{post.body}}</div>
    </div>
</template>

<script>
export default {
    props: {
        posts: {
            type:Array, 
            required: true, 

        }
    }
}
</script>

<style scoped>
.post {
    padding: 1px;
    border: 2px solid teal;
    margin-top: 15px;
    padding: 5px;
}
</style>