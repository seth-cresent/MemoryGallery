<script>
export default {
    data() {
        return {
            image: "image.png",
        }
    }
}
</script>

<template>
    <div class="page-container d-flex flex-column align-items-center">
        <img class="page-bg" src="/image.png" alt="">
        <h1 class="gallery-title text-white">Педагогический состав</h1>

        <div id="officialsCarousel" class="carousel slide custom-carousel" data-bs-ride="carousel">
            <div class="carousel-inner">
                <!-- Карточка учителя 1 -->
                <div class="carousel-item active">
                    <div class="teacher-card mx-auto">
                        <img src="/image.png" alt="Директор" class="teacher-img">
                        <div class="teacher-info">
                            <h3>Иванова Мария Ивановна</h3>
                            <p class="post">Директор школы</p>
                            <p class="description">Почетный работник образования, стаж работы более 25 лет.</p>
                        </div>
                    </div>
                </div>

                <!-- Карточка учителя 2 -->
                <div class="carousel-item">
                    <div class="teacher-card mx-auto">
                        <img src="/image.png" alt="Завуч" class="teacher-img">
                        <div class="teacher-info">
                            <h3>Петров Петр Петрович</h3>
                            <p class="post">Заместитель директора по УВР</p>
                            <p class="description">Учитель истории высшей категории.</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Управление -->
            <button class="carousel-control-prev" type="button" data-bs-target="#officialsCarousel"
                data-bs-slide="prev">
                <span class="carousel-control-prev-icon"></span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#officialsCarousel"
                data-bs-slide="next">
                <span class="carousel-control-next-icon"></span>
            </button>
        </div>
    </div>
</template>

<style scoped>
.page-container {
    min-height: 100vh;
    position: relative;
    padding-bottom: 50px;
}

.page-bg {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    filter: brightness(40%);
    z-index: -1;
}

.custom-carousel {
    width: 100%;
    max-width: 800px;
}

.teacher-card {
    background: #F2ECDF;
    border-radius: 20px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    border: 3px solid #3F2B4C;
}

@media (min-width: 768px) {
    .teacher-card {
        flex-direction: row;
        align-items: stretch;
    }

    .teacher-img {
        width: 300px;
        height: 400px;
    }
}

.teacher-img {
    object-fit: cover;
    border-bottom: 3px solid #3F2B4C;
}

.teacher-info {
    padding: 2rem;
    color: #3F2B4C;
    flex-grow: 1;
}

.teacher-info h3 {
    font-weight: 700;
    color: #3F2B4C;
}

.post {
    font-weight: 600;
    color: #6a4a82;
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
}

.carousel-control-prev,
.carousel-control-next {
    width: 5%;
}
</style>