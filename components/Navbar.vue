<template>
    <nav class="glassy-bg position-fixed d-flex justify-lg-space-between align-center px-16 py-8">
        <div class="primary-gradient text-white px-4 rounded rotate3d">Unappli</div>
        <div class="d-flex" style="gap: 20px">
            <div>Accueil</div>
            <div>Services</div>
            <div>A propos</div>
            <div>Contact</div>
        </div>
    </nav>
</template>

<script setup>

</script>

<style scoped lang="scss">
nav {
    height: 40px;
    width: 100%;
    z-index: 999;
    border-radius: 0;
    .rotate3d {
        animation: rotate3d 10s infinite;
    };
}

@keyframes rotate3d {
    0% {
        transform: rotateY(0deg);
    }
    90% {
        transform: rotateY(0deg);

    }
    100% {
        transform: rotateY(360deg);
    }
}
</style>