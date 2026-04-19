<script>
import { RouterLink } from 'vue-router'
export default {
    data() {
        return {
            image: "image.png"
        }
    }
}
</script>

<template>
    <div class="main-photo">
        <img class="home-page-image" :src="image" alt="">
        <div class="title-container">
            <h1 className="title-text title-heading ">Музей Школы №30</h1>
            <span className="title-text">г.Новоалтайска</span>
            <RouterLink to="/gallery">
                <button class="title-button" :class="classes">Начать исследование</button>
            </RouterLink>
        </div>
    </div>
</template>

<style scoped>
a {
    width: fit-content;
}

.title-container {
    position: absolute;
    top: 30%;
    left: 10%;
    color: #F2ECDF;
    z-index: 2;
    display: flex;
    flex-direction: column;
    gap: 2em;
}

.home-page-image {
    width: 100%;
    height: 100vh;
    user-select: none;
    -webkit-user-drag: none;
    object-fit: cover;
    filter: contrast(105%) brightness(65%)
}

.title-text {
    font-size: 4rem;
    font-weight: 600;
}

.title-heading {
    font-weight: 700;
    font-size: 6rem;
}

.title-button {
    padding: 0.5em 3em;
    background-color: #E0EDAB;
    border: #3F2B4C 2px solid;
    border-radius: 3em;
    font-size: 1.3rem;
    font-weight: 600;
    transition: transform 0.3s ease;

    &:hover {
        transform: scale(1.1);
    }
}

@media (max-width: 1200px) {
    .title-container {
        top: 15%;
        left: 5%;
        right: 5%;
        z-index: 2;
        gap: 1em;
        align-items: center;
        text-align: center;
    }

    .title-button {
        margin-top: 1em;
        padding: 0.5em 1.5em;
        margin-left: 0;
    }

    .title-text {
        font-size: 2rem;
    }

    .title-heading {
        font-size: 3rem;
    }
}
</style>