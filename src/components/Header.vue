<template>
    <header class="header">
        <router-link to="/" class="header__title">Recipes</router-link>
        <ul class=header__links>
            <li><a class="header__link" href="#" v-on:click="$emit('open-popup')">Create Recipe</a></li>
            <li><a class="header__link" href="#">My recipes</a></li>
        </ul>
    </header>
</template>

<script>


export default {
    name: 'Header',
}
</script>

<style scoped>
    .header{
        display: flex;
        align-items: center;
        justify-content: space-around;
        width: 80%;
        padding-bottom: 20px;
        border-bottom: 2px solid #eee;
    }

    @media screen and (max-width: 768) {
        .header{
            width: 70%;
        }
    }

    .header__title{
        font-size: 42px;
        font-weight: bold;
        margin: 0;
        text-decoration: none;
        color: darkslategray;
    }

    .header__links{
        display: flex;
        list-style: none;
        justify-content: space-between;
        width: 270px;
        margin: 0;
    }

    .header__link{
        text-decoration: none;
        color: crimson;
        opacity: 1;
        transition: opacity 0.3s;
    }

    .header__link:hover{
        opacity: 0.6;
    }
</style>