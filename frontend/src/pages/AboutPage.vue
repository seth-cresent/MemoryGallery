<template>
    <div class="page-container d-flex justify-content-center align-items-center">
        <img class="page-bg" src="/image.png" alt="">
        <div class="info-card p-5 text-center">
            <h1 class="mb-4">О нашем музее</h1>
            <p>Школьный музей — это место, где оживает история. Мы бережно храним фотографии, воспоминания и достижения
                наших учеников с момента основания школы.</p>
            <p>Наша цель — сохранить связь поколений и дать возможность каждому выпускнику вновь окунуться в атмосферу
                школьных лет.</p>
        </div>
    </div>
</template>

<style scoped>
.page-container {
    height: 100vh;
    color: #F2ECDF;
}

.page-bg {
    position: fixed;
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    filter: brightness(40%);
    z-index: -1;
}

.info-card {
    background: rgba(63, 43, 76, 0.85);
    border: 2px solid #E0EDAB;
    border-radius: 30px;
    max-width: 800px;
    backdrop-filter: blur(5px);
}
</style>