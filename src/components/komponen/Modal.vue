<template>
    <div class="modal">
        <div class="backdrop" :class="{express: theme === 'astral'}">
            <h1>{{header}}</h1>
            <p>{{text}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['header', 'text', 'theme']
    }
</script>

<style scoped>
    .backdrop p {
        font-style: normal;
    }
    .modal {
        top: 0;
        position: fixed;
        background: rgb(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
    .backdrop {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        color: white;
        background: black;
        border-radius: 10px;
    }
    .backdrop h1 {
        color: white;
    }
    .backdrop.express {
        background-color: crimson;
        color: white;
        font-style: italic;
    }
    .backdrop.backdrop.express h1 {
        border-bottom: 1px solid #ddd;
    }
</style>