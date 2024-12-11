<template>
    <div>
        <h1 :class="classVar">
            Vai corinthians
        </h1>

        <p :class="['text', 'title']">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
             Maiores repellat est quae nostrum ex accusantium quam sequi obcaecati, dolore quo quasi explicabo itaque magni unde repudiandae aliquid molestias! Cum, libero!
        </p>

        <div 
            v-for="obj, index in todos" 
            :key="obj.id"
        >   
            <img
                v-if="obj.imgSrc"
                :src="obj.imgSrc"
            >
            <h1>{{ index }} - {{ obj.title  }}</h1>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
                classVar: 'title',
                pClass: 'text',
                todos: [
                    {
                        "userId": 1,
                        "id": 1,
                        "title": "delectus aut autem",
                        "completed": false,
                        imgSrc: 'https://via.placeholder.com/150',
                    },
                    {
                        "userId": 1,
                        "id": 2,
                        "title": "quis ut nam facilis et officia qui",
                        "completed": false,
                        imgSrc: 'https://via.placeholder.com/150',
                    },
                    {
                        "userId": 1,
                        "id": 3,
                        "title": "fugiat veniam minus",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 4,
                        "title": "et porro tempora",
                        "completed": true
                    },
                    {
                        "userId": 1,
                        "id": 5,
                        "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                        "completed": false
                    }
                ]
            }
        }
    }
</script>

<style>
    .title {
        font-size: 40px;
        color: red; 
    }
    .text {
        font-size: 16px;
        color: blue;
    }
    .header {
        background-color: black;
        color: white;
    }
</style>